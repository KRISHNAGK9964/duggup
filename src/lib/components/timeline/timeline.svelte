<script lang="ts">
  import SteveJobs from "$lib/assets/steveJobs.png";
  import SamAltman from "$lib/assets/samAltman.jpeg";
  import ChevronUpIcon from "$lib/assets/ChevronUpIcon.svg";
  import LogoIcon from "$lib/assets/LogoIcon.svg";
  import setUp from "$lib/assets/setUp.jpeg";
  import map from "$lib/assets/map.png";
  import BetterUp from "$lib/assets/BetterUp.svg";
  const timeLine = [
    {
      profession: {
        designation: "Co-Founder and CEO",
        company: {
          name: "Duggup",
          logo: LogoIcon,
          location: "San Fransisco Bay Area",
        },
        joiningDate: "Nov 2023",
        workLocation: "Remote",
        jobType: "Full-time",
      },
      stories: [
        {
          createdAt: "Dec 2023",
          updatedAt: "Dec 2023",
          storyBanner: SteveJobs,
          story: `No amount of technology can convert a bad story into a good story.`,
        },
        {
          createdAt: "Dec 2023",
          updatedAt: "Dec 2023",
          storyBanner: SamAltman,
          story: `Most people don't have original ideas. Here is how Sam Altman pushes himself to have unpopular ideas.`,
        },
      ],
    },
    {
      profession: {
        designation: "VP Engineering",
        company: {
          name: "BetterUp",
          logo: BetterUp,
          location: "San Fransisco Bay Area",
        },
        joiningDate: "Sep 2022",
        workLocation: "",
        jobType: "Full-time",
      },
      stories: [
        {
          createdAt: "Dec 2023",
          updatedAt: "Dec 2023",
          storyBanner: setUp,
          story: `Startup Lesson I am reflecting. Don't build for the "average person".`,
        },
        {
          createdAt: "Dec 2023",
          updatedAt: "Dec 2023",
          storyBanner: map,
          story: `Your biggest regrets at 80 will be acts of omission.`,
        },
      ],
    },
  ];
</script>

<div
  class="max-w-screen-lg md:mx-auto md:-translate-x-12 lg:mx-auto  lg:-translate-x-24 flex flex-col gap-1 items-center"
>
  {#each timeLine as timeLineElement, index}
    <div class=" w-full grid grid-cols-5">
      <div class=" flex gap-5 col-span-1">
        <p
          class="flex-shrink-0 flex-1 h-min my-auto text-xs leading-4 text-right text-[#7A9299]"
        >
          {timeLineElement.stories[0].updatedAt}
        </p>
        <div class="flex flex-col items-center">
          <div class="flex-1 border-dotted border-r-2 border-[#778FB1]"></div>
          <div class="rounded-full w-4 h-4 border-4 border-[#0066FF]"></div>
          <div class="flex-1 border-dotted border-r-2 border-[#778FB1]"></div>
        </div>
      </div>
      <div
        class="scrollbar-hide col-span-4 flex overflow-auto gap-6 max-h-72 items-center p-6"
      >
        {#each timeLineElement.stories as story}
          <div
            class="flex-1 min-w-72 bg-white flex-col h-full rounded-xl overflow-hidden border-[0.5px] border-[#D0D5DD]"
          >
            <div class="h-[60%] overflow-hidden flex items-center">
              <img
                src={story.storyBanner}
                alt="Steve Jobs"
                class="object-cover"
              />
            </div>
            <div class="h-full p-6">
              <p class="text-sm text-[#141618]">
                {story.story}
              </p>
            </div>
          </div>
        {/each}
      </div>
      <div class="translate-x-1.5 flex gap-5 col-span-1">
        <div class="flex-1 text-right flex flex-col gap-2 justify-center items-end py-4">
          <img
            src={timeLineElement.profession.company.logo}
            alt={`${timeLineElement.profession.company.name} logo`}
            class="w-12 rounded-full overflow-hidden"
          />
          <div class="hidden lg:block">
            <p class="font-bold text-base leading-5 text-[#141618]">
              {timeLineElement.profession.company.name}
            </p>
            <p class="text-xs leading-4 text-[#7A9299]">
              {timeLineElement.profession.company.location}
            </p>
            <p class="text-xs leading-4 text-[#7A9299]">Joined</p>
            <p class="text-xs leading-4 text-[#7A9299]">
              {timeLineElement.profession.joiningDate}
            </p>
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
            {timeLineElement.profession.designation}
          </p>
          <p class="text-[#7A9299] text-xs">
            {timeLineElement.profession.jobType}{timeLineElement.profession
              .workLocation
              ? ` · ${timeLineElement.profession.workLocation}`
              : ""}
          </p>
        </div>
      </div>
    </div>
  {/each}
</div>

<style>
  .scrollbar-hide {
    -ms-overflow-style: none;
    scrollbar-width: none;
  }

  .scrollbar-hide::-webkit-scrollbar {
    display: none;
  }
</style>
