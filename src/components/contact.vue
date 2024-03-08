<template>
  <section class="mx-24 mt-24">
    <div class="mb-10">
      <p class="text-gray-400 tracking-widest pb-1">Contact</p>
      <p class="text-4xl font-bold">Contact Us</p>
    </div>
    <div>
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d26155.417160368233!2d80.13508809996956!3d12.970186614659653!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a525e3510bb6cb3%3A0x8e59bb4c53bf97bc!2sPallavaram%2C%20Chennai%2C%20Tamil%20Nadu!5e0!3m2!1sen!2sin!4v1709786392325!5m2!1sen!2sin" width="100%" height="270" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>
    <div class="flex gap-16 mt-16">
        <div>
            <div class="flex gap-5 mb-8"> 
                <div class=" px-4 mb-1 mt-2 pt-1.5 bg-amber-300 rounded">
                    <i class="icon ion-md-pin text-2xl"></i>
                </div>
                <div>
                    <p class="text-2xl">Location:</p>
                    <p class="text-sm text-gray-500">Pallavaram,Chennai-600043</p>
                </div>
            </div>
            <div class="flex gap-5 mb-8">
                <div class=" px-4 mb-1 mt-2 pt-1.5 bg-amber-300 rounded">
                    <i class="icon ion-ios-mail text-xl"></i>
                </div>
                <div>
                    <p class="text-2xl">Email:</p>
                    <p class="text-sm text-gray-500">info@example.com</p>
                </div>
            </div>
            <div class="flex gap-5">
                <div class=" px-5 mb-1 mt-2 pt-1.5 bg-amber-300 rounded">
                    <i class="icon ion-ios-phone-portrait text-xl"></i>
                </div>
                <div>
                    <p class="text-2xl">Call:</p>
                    <p class="text-sm text-gray-500">+91 9876543210</p>
                </div>
            </div>
        </div>
        <div class="w-[700px]">
            <form>
                <div class="flex gap-6 mb-5 mt-1">
                    <div>
                        <input class="outline-none border border-gray-500 rounded h-10 w-[338px] px-5 text-sm" type="text" name="name" id="name" placeholder="Your Name" required>
                    </div>
                    <div>
                        <input class="outline-none border border-gray-500 rounded h-10 w-[338px]  px-5 text-sm" type="email" name="email" id="email" placeholder="Your Email" required>
                    </div>
                </div>
                <div class="mb-5"> 
                    <input class="outline-none border border-gray-500 rounded h-10 w-full  px-5 text-sm" type="text" name="subject" id="subject" placeholder="Subject" required>
                </div>
                <div>
                    <textarea class="outline-none border border-gray-500 rounded w-full h-24  px-5 text-sm pt-4" name="message" id="message" placeholder="Message" required></textarea>
                </div>
                <div class="text-center mt-4">
                    <button type="submit" class="bg-amber-400 px-4 py-2 rounded">Send message</button>
                </div>                
            </form>
        </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
input:focus,
textarea:focus{
    border-color: #ffc451;
}
.bg-amber-400{
    transition: 0.5s;
}
.bg-amber-400:hover{
    background-color: #ffc451;
}
</style>