+++
title = “Rahul”
[extra]
scripts = [“js/home.js”, “js/shy.js”]
no_header = true
socials = [
{ name = “Reddit”, url = “https://www.reddit.com/user/praizeTheFool/”, icon = “/social-icons/16x/reddit_icon_bg.png” },
{ name = “Instagram”, url = “https://www.instagram.com”, icon = “/social-icons/16x/instagram_icon_bg.png” },
]
forges = [
{ name = “GitHub”, url = “https://github.com/notcandy001”, icon = “/social-icons/16x/github_icon_bg.png” },
]
contacts = [
{ name = “Discord”, url = “https://discord.com/channels/1396466557760176280/1396466558313693196”, icon = “/social-icons/16x/discord_icon_bg.png” },
{ name = “Email”, url = “mailto:candynot8@gmail.com”, icon = “/social-icons/16x/domain_icon_bg.png” },
]
+++

<section class="snap-section hero-wrapper">
<div class="hero-container">
<div class="hero-content">
{{ retro_text(text="Rahul", tag="h1") }}
<p style="font-size: 1rem; margin-bottom: 2rem; line-height: 1.6;">
I'm <mark>Rahul</mark>. You probably know me as <mark>notcandy001</mark> or <mark>praizeTheFool</mark>. Second year Computer Science student exploring Linux internals, system configuration, and tools I build from scratch not to move faster but to understand systems deeply.
</p>
</div>

{{ retro_avatar(src=”/images/avatar.png”, alt=“Rahul”) }}

</div>
<div id="scroll-target" style="position: absolute; bottom: 110px; left: 50%; width: 1px; height: 1px; z-index: -1;"></div>

<a class="scroll-indicator" href="#about" style="position: absolute; bottom: 120px; left: 50%; margin-left: -120px; display: flex; align-items: flex-end; gap: 76px; pointer-events: auto; cursor: pointer; z-index: 10; text-decoration: none;">
<div style="width: 96px; height: 96px; z-index: 0; animation: svg-boil 0.3s infinite steps(1); flex-shrink: 0;">
<div class="axie-icon" style="width: 96px; height: 96px; background-color: var(--accent-color); -webkit-mask: url('/images/axie.svg') no-repeat center / contain; mask: url('/images/axie.svg') no-repeat center / contain; transition: background-color 0.3s ease;"></div>
</div>
<div style="margin-bottom: 28px; min-width: max-content;">
<div style="transform: rotate(5deg); display: inline-block; text-align: center;">
{{ arrow_note(text="Pssst...<br>There's more.", target="scroll-target", start_dir="left", end_dir="top", color="accent", font_size="1rem", amplitude="30", spacing="10", stroke_width="2") }}
</div>
</div>
</a>
</section>

<script>
  const scrollIndicator = document.querySelector('.scroll-indicator');
  if (scrollIndicator) {
    const axie = scrollIndicator.querySelector('.axie-icon');
    scrollIndicator.addEventListener('mouseenter', () => {
      const paths = document.querySelectorAll('.arrow-path-boil');
      paths.forEach(p => { p.style.transition = 'stroke 0.3s ease'; p.style.stroke = 'var(--fg-color)'; });
      if (axie) axie.style.backgroundColor = 'var(--fg-color)';
      const note = scrollIndicator.querySelector('.arrow-note');
      if (note) { note.style.transition = 'color 0.3s ease'; note.style.color = 'var(--fg-color)'; }
    });
    scrollIndicator.addEventListener('mouseleave', () => {
      const paths = document.querySelectorAll('.arrow-path-boil');
      paths.forEach(p => { p.style.stroke = 'var(--accent-color)'; });
      if (axie) axie.style.backgroundColor = 'var(--accent-color)';
      const note = scrollIndicator.querySelector('.arrow-note');
      if (note) { note.style.color = 'var(--accent-color)'; }
    });
  }
</script>

<section class="snap-section content-wrapper">
<div style="width: 100%;">

## About

<ul class="masonry">
<li>
<article>

<img src="/images/space.gif" style="height:128px; width:100%; object-fit:cover; object-position:center;">

**I build things to understand them.**

**I’m {{ age() }} years old.**

I was born September 12, 2006. Since then I’ve been curious about how things actually work beneath the surface. While most people are happy just using software, I like digging deeper into the kernel, the compositor, the configs, and the systems that make everything run.

For me, understanding a system is more interesting than simply using it. I want to know why something works, not just that it works.

Outside of computers, I enjoy cliff jumping, swimming, diving, trekking with friends, bike and car rides, gaming, and all kinds of outdoor fun. Currently playing BGMI and Wuthering Waves.

</article>

<article class="fancy-list">

**✨ Areas of Focus:**

- Linux internals
- Hyprland customization
- TypeScript
- HTML & CSS
- Git
- QML (learning)
- Language design
- C++ (planning to learn)

</article>

<article>

{{ github_grid(username=“notcandy001”, color=”#40c463”) }}

I genuinely enjoy coding and problem-solving. There’s something satisfying about understanding exactly why something works not just that it works. :)

</article>
</li>

<li>
<article>

**👾 I study Computer Science.**

My curiosity about how computers actually work led me here. I get to dig into the things I’ve always wondered about — OS internals, language design, how abstractions are built from the ground up.

</article>

<article>

**🔧 I like tinkering and building custom tools.**

I’m obsessed with building my own tools and workflows. People say not to reinvent the wheel, but I think custom tools can unlock freedom and a deeper understanding. Just like every person is unique, the tools they use can be too. :D

</article>

<article class="fancy-list anime">

**🎌 Anime I’ve watched:**

{{ anime() }}

</article>
</li>
</ul>

</div>

## Online

Where and when to find me online.

<ul class="masonry">
<li>
{{ now_playing() }}
</li>

<li>
<article class="online fancy-list">
<strong id="socials" class="title">Socials</strong>
{{ online(type="socials") }}
</article>
</li>

<li>
<article class="online fancy-list">
<strong id="forges" class="title">Code</strong>
{{ online(type="forges") }}
</article>
</li>

<li>
<article class="online fancy-list">
<strong id="contacts" class="title">Contacts</strong>

For me it’s currently <mark><time id="clock">00:00</time></mark> <small>(IST)</small> and I’m <span id="online-indicator"><i class="icon"></i><span id="online-indicator-text">Offline</span></span>.

Feel free to reach out on any of these!

{{ online(type=“contacts”) }}

</article>
</li>
</ul>

</section>
