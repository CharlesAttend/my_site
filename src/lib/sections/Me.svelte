<script>
  import pp from "$lib/assets/pp.webp";
  import git_icon from "$lib/assets/git_icon.svg";
  import linkedin_icon from "$lib/assets/linkedin_icon.svg";
  // import resume_icon from "$lib/assets/resume_icon.svg";
  import envelope_icon from "$lib/assets/envelope_icon.svg";
  import bsky_icon from "$lib/assets/bsky_icon.svg";
  const link_list = [
    {
      href: "https://github.com/CharlesAttend/",
      img: git_icon,
      alt: "github_icon",
      text: "CharlesAttend",
      title: "My GitHub",
    },
    {
      href: "https://bsky.app/profile/charles.vin",
      img: bsky_icon,
      alt: "bsky_icon",
      text: "Charles Vin",
      title: "My BlueSky profile",
    },
    {
      href: "https://linkedin.com/in/charles-vin/",
      img: linkedin_icon,
      alt: "linkedin_icon",
      text: "Charles Vin",
      title: "My LinkedIn",
    },
    {
      href: "mailto:charles.vin@outlook.fr",
      img: envelope_icon,
      alt: "mail_icon",
      text: "charles.vin@outlook.fr",
      title: "My mail",
    },
    // update grid length accordingly, automatic update slow down the page
    // { href: "", img: resume_icon, alt: "envelope_icon", text: "Resume" },
  ];
</script>

<div
  class="my-5 inline-flex w-full flex-col items-center justify-center gap-2.5 overflow-hidden sm:max-w-xl"
>
  <img class="w-2/3 max-w-sm rounded-full shadow-lg" src={pp} alt="Me" />
  <!-- <h2 class="text-center">Usefull links</h2> -->
  <div class="grid w-full grid-cols-4 justify-items-center gap-5">
    {#each link_list as link}
      <a
        href={link.href}
        title={link.title}
        target="_blank"
        rel="noreferrer noopener"
        class="inline-flex items-center rounded-lg px-4 py-2 text-mauve-900 hover:bg-mauve-100 hover:text-blue-700 focus:z-10 focus:text-blue-700 focus:outline-none focus:ring-4 focus:ring-mauve-200"
      >
        <img class="w-7 lg:w-8 xl:w-9" src={link.img} alt={link.alt} />
      </a>
    {/each}
  </div>
</div>
