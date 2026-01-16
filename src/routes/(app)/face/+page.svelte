<script lang="ts">
  import { onMount, onDestroy } from 'svelte';

  let videoElement: HTMLVideoElement;
  let canvasElement: HTMLCanvasElement;
  let stream: MediaStream | null = null;
  let capturedImage: string | null = null;
  let errorMsg: string = '';

  // 1. ฟังก์ชันเปิดกล้อง
  async function startCamera() {
    try {
      // ขอสิทธิ์เข้าถึงกล้อง (video: true)
      stream = await navigator.mediaDevices.getUserMedia({
        video: { facingMode: 'user' } // 'user' = กล้องหน้า, 'environment' = กล้องหลัง
      });
      
      // เอา Stream ใส่เข้าไปใน <video>
      if (videoElement) {
        videoElement.srcObject = stream;
      }
      errorMsg = '';
    } catch (err) {
      console.error("Error accessing camera:", err);
      errorMsg = 'ไม่สามารถเข้าถึงกล้องได้ กรุณาอนุญาตสิทธิ์การใช้งาน';
    }
  }

  // 2. ฟังก์ชันถ่ายรูป
  function capturePhoto() {
    if (!videoElement || !canvasElement) return;

    // กำหนดขนาด canvas ให้เท่ากับขนาดวิดีโอจริง
    const width = videoElement.videoWidth;
    const height = videoElement.videoHeight;
    canvasElement.width = width;
    canvasElement.height = height;

    // วาดภาพจาก <video> ลงบน <canvas>
    const context = canvasElement.getContext('2d');
    if (context) {
      context.drawImage(videoElement, 0, 0, width, height);
      
      // แปลง canvas เป็นรูปภาพ (Base64)
      capturedImage = canvasElement.toDataURL('image/png');
    }
  }

  // 3. ฟังก์ชันปิดกล้อง (Clear Memory)
  function stopCamera() {
    if (stream) {
      stream.getTracks().forEach(track => track.stop());
      stream = null;
    }
    if (videoElement) {
      videoElement.srcObject = null;
    }
  }

  // เริ่มเปิดกล้องเมื่อหน้าเว็บโหลดเสร็จ
  onMount(() => {
    startCamera();
  });

  // อย่าลืมปิดกล้องเมื่อเปลี่ยนหน้า เพื่อไม่ให้กล้องค้าง
  onDestroy(() => {
    stopCamera();
  });
</script>

<div class="flex flex-col items-center gap-4 p-4">
  <h1 class="text-xl font-bold">📷 กล้องถ่ายรูป SvelteKit</h1>

  {#if errorMsg}
    <p class="text-red-500">{errorMsg}</p>
  {/if}

  <div class="relative w-full max-w-md bg-black rounded-lg overflow-hidden shadow-lg">
    <video 
      bind:this={videoElement} 
      autoplay 
      playsinline 
      class="w-full h-auto"
    ></video>
  </div>

  <div class="flex gap-4">
    {#if !capturedImage}
      <button 
        on:click={capturePhoto} 
        class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700 font-bold shadow-md"
      >
        ถ่ายรูป
      </button>
    {:else}
      <button 
        on:click={() => { capturedImage = null; }} 
        class="bg-gray-600 text-white px-6 py-2 rounded-full hover:bg-gray-700"
      >
        ถ่ายใหม่
      </button>
    {/if}
  </div>

  <canvas bind:this={canvasElement} class="hidden"></canvas>

  {#if capturedImage}
    <div class="mt-4 text-center">
      <p class="text-sm text-gray-500 mb-2">รูปที่บันทึกได้:</p>
      <img src={capturedImage} alt="Captured" class="w-full max-w-xs rounded-lg border border-gray-300 shadow-sm" />
      
      <a 
        href={capturedImage} 
        download="my-photo.png" 
        class="inline-block mt-2 text-blue-500 underline"
      >
        ดาวน์โหลดรูปภาพ
      </a>
    </div>
  {/if}
  <input type="file" accept="image/*" capture="user" />
</div>