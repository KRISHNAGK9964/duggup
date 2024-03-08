<script lang="ts">
  import LogoIcon from "$lib/assets/LogoIcon.svg";
  import LogoText from "$lib/assets/LogoText.svg";
  import ProfileImage from "$lib/assets/Profile2.png";
  import ChevronDown from "$lib/assets/ChevronDown.svg";
  import PlusIcon from "$lib/assets/PlusIcon.svg";
  import HomeIcon from "$lib/assets/HomeIcon.svg";
  import StoryIcon from "$lib/assets/StoryIcon.svg";
  import BookIcon from "$lib/assets/BookIcon.svg";
</script>

<div
  class="nav max-w-screen-xl w-full px-2 xl:px-0 flex justify-between mx-auto border-dotted border-b-2"
>
  <div class="flex items-center gap-1">
    <img src={LogoIcon} alt="duggup logo icon" class="w-7 h-7" />
    <img src={LogoText} alt="duggup" class="hidden md:block" />
  </div>
  <div class="nav-right flex gap-5 md:gap-7 lg:gap-10 items-center">
    <div class="flex border-black gap-5 md:gap-7 lg:gap-10 items-center">
      <div class="flex gap-5 md:gap-7 lg:gap-10 border-black">
        <div class="flex items-center border-black">
          <div class="p-1 border-black flex items-center justify-center">
            <img src={HomeIcon} alt="Home Icon" class="w-6" />
          </div>
          <p class="p-2 hidden sm:block">Home</p>
        </div>
        <div class="flex items-center">
          <div class="p-1 flex items-center justify-center">
            <img src={StoryIcon} alt="Home Icon" class="w-6" />
          </div>
          <div class="p-2 hidden sm:block">Explore</div>
        </div>
        <div class="flex items-center">
          <div class="p-1 flex items-center justify-center">
            <img src={BookIcon} alt="Home Icon" class="w-6" />
          </div>
          <div class="p-2 hidden sm:block">Learn</div>
        </div>
      </div>
      <div
        class=" max-h-9 h-fit border-[0.5px] border-[#4D4D4D] shadow-[0_4px_0_0_#4D4D4D] rounded px-1 sm:px-2 md:px-3 lg:px-4 bg-white flex items-center"
      >
        <div class="p-1 flex items-center justify-center">
          <img src={PlusIcon} alt="Plus Icon" class="w-4 h-4" />
        </div>
        <div class="w-[46px] p-2">Post</div>
      </div>
    </div>
    <div class="profile pr-2 lg:px-3 py-3 gap-1 flex items-center">
      <div
        class="rounded-full h-12 w-12 border-[0.5px] border-[#4D4D4D] overflow-clip"
      >
        <img
          src={ProfileImage}
          alt="user profile"
          class="object-cover scale-105"
        />
      </div>
      <div class="hidden md:block line-clamp-1 overflow-ellipsis text-nowrap">
        Krishna Kiran
      </div>
      <div class="hidden md:flex w-4 h-4 items-center justify-center">
        <img src={ChevronDown} alt="chevron-down icon" class="object-contain" />
      </div>
    </div>
  </div>
</div>
