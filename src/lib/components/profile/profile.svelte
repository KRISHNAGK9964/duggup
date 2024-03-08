<script lang="ts">
  import Profile2 from "$lib/assets/Profile2.png";
  import Logo2Icon from "$lib/assets/Logo2Icon.svg";
  import LinkIcon from "$lib/assets/LinkIcon.svg";
  import ThreeDotsIcon from "$lib/assets/ThreeDotsIcon.svg";
</script>

<div class="flex mx-auto p-8 max-w-screen-lg gap-8 md:gap-12">
  <div class="flex flex-col items-center">
    <div class="flex items-center justify-center rounded-full overflow-clip">
      <img src={Profile2} alt="User Profile" class="cursor-pointer" />
    </div>
    <p class="font-bold text-[24px] text-lg text-center text-[#4B5C6D] underline-offset-1 cursor-pointer hover:underline decoration-2 decoration-blue-500">
      Krishna <br /> Kiran
    </p>
  </div>
  <div class="flex-1 flex flex-col py-4 gap-5">
    <div class="flex justify-between">
      <p class="w-3/4 font-normal text-[14px] text-base text-[#141618]">
        Co-Founder and CEO at Duggup - Social network for people in tech.
        Ex-Amazon Head of Engineering. I write hot-takes on building a business,
        shipping delightful products and accelerating product and career growth.
      </p>
      <div class="  flex flex-col gap-2 items-end">
        <img
          src={Logo2Icon}
          alt="Duggup icon"
          class="w-9 h-9 rounded-full overflow-hidden cursor-pointer"
        />

        <div class="text-right flex flex-col gap-1">
          <p class="font-bold text-black text-[1rem] leading-5 cursor-pointer hover:underline underline-offset-1 decoration-sky-500">Diggup</p>
          <p class="text-right text-xs leading-3 text-[#7A9299]">
            Co-Founder and CEO
          </p>
        </div>
      </div>
    </div>
    <div class="flex justify-between">
      <div class=" flex items-center">
        <button
          class="p-2 max-h-9 rounded px-4 bg-white hover:bg-[#0066FF] hover:text-white border-[0.5px] border-[#4D4D4D] hover:border-[#0066FF] shadow-[0_4px_0_0_#4D4D4D] hover:shadow-[0_4px_0_0_#003A91]"
          >Followed</button
        >
      </div>
      <div class="flex items-center gap-4 pl-4">
        <div class="flex items-center gap-1 text-[#4D4D4D] cursor-pointer">
          <span class="text-sm leading-5 text-[#4D4D4D]">My website</span>
          <img src={LinkIcon} alt="Link icon" class="w-3 h-3" />
        </div>
        <img
          src={ThreeDotsIcon}
          alt="ThreeDots Icon"
          class="text-[#A5B9D3] w-7 h-7 cursor-pointer"
        />
      </div>
    </div>
  </div>
</div>
