<script lang="ts">
  import Profile2 from "$lib/assets/Profile2.png";
  import Logo2Icon from "$lib/assets/Logo2Icon.svg";
  import LinkIcon from "$lib/assets/LinkIcon.svg";
  import ThreeDotsIcon from "$lib/assets/ThreeDotsIcon.svg";
  import type { ButtonEvents } from "svelte-radix/Button.svelte";
  let following = ["1234"];
  const profile = {
    _id: "1234",
    profileImage: Profile2,
    userName: { firstName: "Krishna", lastName: "Kiran" },
    profileHeader:
      "Co-Founder and CEO at Duggup - Social network for people in tech. Ex-Amazon Head of Engineering. I write hot-takes on building a business, shipping delightful products and accelerating product and career growth.",
    profession: {
      designation: "Co-Founder and CEO",
      company: {
        name: "Duggup",
        logo: Logo2Icon,
      },
    },
    links: {
      webSite: "http://localhost:5173",
    },
  };
  let isFollowing = following.includes(profile._id);
  const followHandler = (profileId: string) => {
    console.log(following, profileId);
    if (isFollowing) {
      following = following.filter((id) => id !== profileId);
    } else {
      following.push(profileId);
    }
    isFollowing = !isFollowing;
  };
</script>

<div class="flex mx-auto p-8 max-w-screen-lg gap-8 md:gap-12">
  <div class="flex flex-col items-center">
    <div class="flex items-center justify-center rounded-full overflow-clip">
      <img
        src={profile.profileImage}
        alt="User Profile"
        class="cursor-pointer"
      />
    </div>
    <p
      class="font-bold text-[24px] text-lg text-center text-[#4B5C6D] underline-offset-1 cursor-pointer hover:underline decoration-2 decoration-blue-500"
    >
      {profile.userName.firstName} <br />
      {profile.userName.lastName}
    </p>
  </div>
  <div class="flex-1 flex flex-col py-4 gap-5">
    <div class="flex justify-between">
      <p class="w-3/4 font-normal text-[14px] text-base text-[#141618]">
        {profile.profileHeader}
      </p>
      <div class="  flex flex-col gap-2 items-end">
        <img
          src={profile.profession.company.logo}
          alt="Duggup icon"
          class="w-9 h-9 rounded-full overflow-hidden cursor-pointer"
        />

        <div class="text-right flex flex-col gap-1">
          <p
            class="font-bold text-black text-[1rem] leading-5 cursor-pointer hover:underline underline-offset-1 decoration-sky-500"
          >
            {profile.profession.company.name}
          </p>
          <p class="text-right text-xs leading-3 text-[#7A9299]">
            {profile.profession.designation}
          </p>
        </div>
      </div>
    </div>
    <div class="flex justify-between">
      <div class=" flex items-center">
        {#key following}
          <button
            on:click={(e) => followHandler(profile._id)}
            class="p-2 max-h-9 rounded px-4 bg-white hover:bg-[#0066FF] hover:text-white border-[0.5px] border-[#4D4D4D] hover:border-[#0066FF] shadow-[0_4px_0_0_#4D4D4D] hover:shadow-[0_4px_0_0_#003A91]"
            >{isFollowing ? "Followed" : "Follow"}</button
          >
        {/key}
      </div>
      <div class="flex items-center gap-4 pl-4">
        <a
          href={profile.links.webSite}
          target="_blank"
          rel="noopener noreferrer"
        >
          <div class="flex items-center gap-1 text-[#4D4D4D] cursor-pointer">
            <span class="text-sm leading-5 text-[#4D4D4D]">My website</span>
            <img src={LinkIcon} alt="Link icon" class="w-3 h-3" />
          </div>
        </a>
        <img
          src={ThreeDotsIcon}
          alt="ThreeDots Icon"
          class="text-[#A5B9D3] w-7 h-7 cursor-pointer"
        />
      </div>
    </div>
  </div>
</div>
