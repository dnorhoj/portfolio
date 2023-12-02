<script lang="ts">
  import {
    faGithub,
    faDiscord,
    faLinkedin,
    faTwitter,
    faYoutube,
    faMastodon,
  } from "@fortawesome/free-brands-svg-icons";

  import Swal from "sweetalert2";
  import Icon from "$lib/components/icon.svelte";
</script>

<div {...$$props}>
  <Icon href="https://github.com/dnorhoj" icon={faGithub} />
  <Icon
    icon={faDiscord}
    callback={(e) => {
      e?.preventDefault;
      Swal.fire({
        title: "Discord",
        html: "Add me on discord! <b>dnorhoj</b>",
        showCancelButton: true,
        confirmButtonText: "Copy",
      }).then((result) => {
        if (result.isConfirmed) {
          navigator.clipboard.writeText("dnorhoj");
        }
      });
    }}
  />
  <Icon href="https://www.linkedin.com/in/daniel-norhoj/" icon={faLinkedin} />
  <Icon href="https://fosstodon.org/@dnorhoj" icon={faMastodon} />
  <Icon href="https://twitter.com/dnorhoj" icon={faTwitter} />
  <Icon href="https://youtu.be/dQw4w9WgXcQ" icon={faYoutube} />
</div>
