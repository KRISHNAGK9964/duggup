<script lang="ts">
  import Nav from "$lib/components/nav/nav.svelte";
  import Profile from "$lib/components/profile/profile.svelte";
  import TimeLine from "$lib/components/timeline/timeline.svelte";
  import SteveJobs from "$lib/assets/SteveJobs.png";
  import SamAltman from "$lib/assets/samAltman.jpeg";
  import ChevronUpIcon from "$lib/assets/ChevronUpIcon.svg";
  import LogoIcon from "$lib/assets/LogoIcon.svg";
  import setUp from "$lib/assets/setUp.jpeg";
  import map from "$lib/assets/map.png";
  import BetterUp from "$lib/assets/BetterUp.svg";
</script>

<div class="w-full min-h-screen bg-[#FCFCFF]">
  <Nav />
  <Profile />
  <TimeLine />
  <!-- <div
    class="max-w-screen-lg mx-auto md:-translate-x-12 lg:-translate-x-24 overflow-hidden flex flex-col gap-1 items-center"
  >
    <div class=" w-full grid grid-cols-5">
      <div class="px-2 flex gap-5">
        <p
          class="flex-shrink-0 flex-1 h-min my-auto text-xs leading-4 text-right text-[#7A9299]"
        >
          Dec 2023
        </p>
        <div class="flex flex-col items-center">
          <div class="flex-1 border-dotted border-r-2 border-[#778FB1]"></div>
          <div class="rounded-full w-4 h-4 border-4 border-[#0066FF]"></div>
          <div class="flex-1 border-dotted border-r-2 border-[#778FB1]"></div>
        </div>
      </div>
      <div
        class="col-span-4 flex gap-6 max-h-72 items-center justify-center p-6"
      >
        <div
          class="flex-1 flex-col h-full rounded-xl overflow-hidden border-[0.5px] border-[#D0D5DD]"
        >
          <div class="h-[60%] overflow-hidden flex items-center">
            <img src={SteveJobs} alt="Steve Jobs" class="object-cover" />
          </div>
          <div class="h-full p-6">
            <p class="text-sm text-[#141618]">
              No amount of technology can convert a bad story into a good story.
            </p>
          </div>
        </div>
        <div
          class="flex-1 flex-col h-full rounded-xl overflow-hidden border-[0.5px] border-[#D0D5DD]"
        >
          <div class="h-[60%] w-full overflow-hidden flex items-center">
            <img src={SamAltman} alt="Steve Jobs" class="object-cover" />
          </div>
          <div class="p-6">
            <p class="text-sm text-[#141618] line-clamp-3 text-ellipsis">
              Most people don't have original ideas. Here is how Sam Altman
              pushes himself to have unpopular ideas.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="grid grid-cols-5 w-full">
      <div class="px-0.5 flex gap-5">
        <div class="flex-1 text-right flex flex-col gap-2 items-end py-4">
          <img
            src={LogoIcon}
            alt="Diggup Logo Icon"
            class="w-12 h-12 rounded-full overflow-hidden"
          />
          <div class="">
            <p class="font-bold text-base leading-5 text-[#141618]">Duggup</p>
            <p class="text-xs leading-4 text-[#7A9299]">
              San Fransisco Bay Area
            </p>
            <p class="text-xs leading-4 text-[#7A9299]">Joined</p>
            <p class="text-xs leading-4 text-[#7A9299]">Nov 2023</p>
          </div>
        </div>
        <div class="flex flex-col items-center">
          <img src={ChevronUpIcon} alt="chevron up icon" />
          <div class="flex-1 border-dotted border-r-2 border-[#778FB1]"></div>
          <div class="rounded-full w-7 h-7 border-8 border-[#0066FF]"></div>
          <div class="flex-1 border-dotted border-r-2 border-[#778FB1]"></div>
        </div>
      </div>
      <div class="col-span-4 w-full flex items-center px-6">
        <div
          class="bg-white shadow-[0px_1px_2px_0px_#DBE5F540] w-full rounded-xl py-4 px-5 flex flex-col gap-1"
        >
          <p class="font-bold text-xl leading-8 text-[#141618]">
            Co-Founder and CEO
          </p>
          <p class="text-[#7A9299] text-xs">Full-time · Remote</p>
        </div>
      </div>
    </div>
    <div class=" w-full grid grid-cols-5">
      <div class="px-2 flex gap-5">
        <p
          class="flex-shrink-0 flex-1 h-min my-auto text-xs leading-4 text-right text-[#7A9299]"
        >
          Dec 2023
        </p>
        <div class="flex flex-col items-center">
          <div class="flex-1 border-dotted border-r-2 border-[#778FB1]"></div>
          <div class="rounded-full w-4 h-4 border-4 border-[#0066FF]"></div>
          <div class="flex-1 border-dotted border-r-2 border-[#778FB1]"></div>
        </div>
      </div>
      <div
        class="col-span-4 flex gap-6 max-h-72 items-center justify-center p-6"
      >
        <div
          class="flex-1 flex-col h-full rounded-xl overflow-hidden border-[0.5px] border-[#D0D5DD]"
        >
          <div class="h-[60%] overflow-hidden flex items-center">
            <img src={setUp} alt="setUp" class="object-cover" />
          </div>
          <div class="h-full p-6">
            <p class="text-sm text-[#141618]">
              Startup Lesson I am reflecting. Don't build for the "average person".
            </p>
          </div>
        </div>
        <div
          class="flex-1 flex-col h-full rounded-xl overflow-hidden border-[0.5px] border-[#D0D5DD]"
        >
          <div class="h-[60%] w-full overflow-hidden flex items-center">
            <img src={map} alt="old map" class="object-cover" />
          </div>
          <div class="p-6">
            <p class="text-sm text-[#141618] line-clamp-3 text-ellipsis">
              Your biggest regrets at 80 will be acts of omission.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="grid grid-cols-5 w-full">
      <div class="px-0.5 flex gap-5">
        <div class="flex-1 text-right flex flex-col gap-2 items-end py-4">
          <img
            src={BetterUp}
            alt="Diggup Logo Icon"
            class="w-12 h-12 rounded-full overflow-hidden"
          />
          <div class="">
            <p class="font-bold text-base leading-5 text-[#141618]">BetterUp</p>
            <p class="text-xs leading-4 text-[#7A9299]">
              San Fransisco Bay Area
            </p>
            <p class="text-xs leading-4 text-[#7A9299]">Joined</p>
            <p class="text-xs leading-4 text-[#7A9299]">Sep 2022</p>
          </div>
        </div>
        <div class="flex flex-col items-center">
          <img src={ChevronUpIcon} alt="chevron up icon" />
          <div class="flex-1 border-dotted border-r-2 border-[#778FB1]"></div>
          <div class="rounded-full w-7 h-7 border-8 border-[#0066FF]"></div>
          <div class="flex-1 border-dotted border-r-2 border-[#778FB1]"></div>
        </div>
      </div>
      <div class="col-span-4 w-full flex items-center px-6">
        <div
          class="bg-white shadow-[0px_1px_2px_0px_#DBE5F540] w-full rounded-xl py-4 px-5 flex flex-col gap-1"
        >
          <p class="font-bold text-xl leading-8 text-[#141618]">
            VP Engineering
          </p>
          <p class="text-[#7A9299] text-xs">Full-time</p>
        </div>
      </div>
    </div>
  </div> -->
</div>
