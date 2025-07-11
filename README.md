<style>
  /* Basic Styling for Layout and Colors */
  :root {
    --primary-color: #3498db;
    --secondary-color: #2ecc71;
    --text-color: #2c3e50;
    --light-text-color: #7f8c8d;
    --bg-light: #fdfdfd;
    --card-bg: #ffffff;
    --shadow-light: rgba(0,0,0,0.05);
    --shadow-medium: rgba(0,0,0,0.1);
  }

  body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol"; color: var(--text-color); }

  h1, h2, h3, h4, h5, h6 { color: var(--text-color); }
  p { color: var(--light-text-color); }
  a { color: var(--primary-color); text-decoration: none; }

  /* Animated Skill Icons (Tailwind-like hover effects) */
  .animated-skill {
    transition: transform 0.3s ease-in-out, filter 0.3s ease-in-out;
  }
  .skill-item:hover .animated-skill {
    transform: translateY(-5px) scale(1.05); /* lifted and slightly larger */
    filter: drop-shadow(0 5px 10px var(--shadow-medium)); /* subtle shadow */
  }

  /* Tooltip text styling (CSS-only basic tooltip) */
  .tooltip-text {
    visibility: hidden;
    width: 160px;
    background-color: #333;
    color: #fff;
    text-align: center;
    border-radius: 6px;
    padding: 8px 0;
    position: absolute;
    z-index: 1;
    bottom: 125%; /* Position above the icon */
    left: 50%;
    margin-left: -80px; /* Center the tooltip */
    opacity: 0;
    transition: opacity 0.3s ease-in-out, visibility 0.3s ease-in-out;
    font-size: 0.85em;
    box-shadow: 0 2px 8px var(--shadow-medium);
  }
  .skill-item:hover .tooltip-text {
    visibility: visible;
    opacity: 1;
  }
  /* Tooltip arrow */
  .tooltip-text::after {
    content: " ";
    position: absolute;
    top: 100%; /* At the bottom of the tooltip */
    left: 50%;
    margin-left: -5px;
    border-width: 5px;
    border-style: solid;
    border-color: #333 transparent transparent transparent;
  }

  /* Animated Buttons (Tailwind-like hover effects) */
  .animated-button {
    display: inline-block;
    padding: 10px 25px;
    border-radius: 8px;
    font-weight: bold;
    text-decoration: none;
    transition: all 0.3s ease;
    box-shadow: 0 4px 10px var(--shadow-light);
  }
  .animated-button:hover {
    transform: translateY(-2px); /* Subtle lift */
    box-shadow: 0 6px 15px var(--shadow-medium); /* Enhanced shadow */
  }
  .live-demo { background-color: var(--secondary-color); color: white; }
  .live-demo:hover { background-color: #27ae60; } /* Darker green on hover */
  .view-code { background-color: var(--primary-color); color: white; }
  .view-code:hover { background-color: #2980b9; } /* Darker blue on hover */
  .animated-contact-button { background-color: var(--primary-color); color: white; border-radius: 50px; }
  .animated-contact-button:hover { background-color: #2980b9; transform: translateY(-3px) scale(1.02); box-shadow: 0 8px 20px rgba(52, 152, 219, 0.4); }

  /* Animated Social Icons (Tailwind-like hover effects) */
  .animated-social-icon {
    transition: transform 0.3s ease-in-out, filter 0.3s ease-in-out;
  }
  .animated-social-icon:hover {
    transform: scale(1.1) rotate(5deg); /* Slightly larger and rotated */
    filter: saturate(1.5) brightness(1.1); /* More vibrant */
  }

  /* Section Dividers - conceptual as a background SVG/GIF */
  .section-divider {
    width: 100%;
    height: 50px;
    object-fit: contain;
    margin: 50px 0;
    opacity: 0.7;
  }

  /* Card styling */
  .card-style {
    background: var(--card-bg);
    border-radius: 12px;
    box-shadow: 0 8px 25px var(--shadow-light);
    overflow: hidden;
  }

  /* Specific animations for dynamic sections (via GitHub Actions generating SVGs/content) */
  @keyframes fill-animation {
    from { width: 0%; }
    to { width: var(--fill-percentage, 100%); } /* Controlled by inline style/GitHub Action */
  }

  /* Adjust for better mobile responsiveness */
  @media (max-width: 768px) {
    .skill-grid { grid-template-columns: repeat(auto-fit, minmax(80px, 1fr)); gap: 20px; }
    .skill-item img { width: 60px; height: 60px; }
    .project-card { flex: 0 0 90%; }
    .dynamic-section { width: 100%; margin: 10px 0; }
  }
</style>

<div align="center">
  <h1 id="hero-title" style="font-size: 3.5em; margin-bottom: 0.1em; color: var(--text-color);">
    Hi, I'm <span class="typewriter" style="font-weight: bold; color: var(--primary-color);" data-words='["Ahmed Aaliyan", "a Front-End Architect", "an Interactive Experiences Specialist", "a Pixel-Perfect Crafter"]'></span>
  </h1>
  <p style="font-size: 1.2em; color: var(--light-text-color);">Crafting immersive and performance-driven web interfaces.</p>

  <img src="https://64.media.tumblr.com/f9a888a75e3a0b3f52b0d0a7a0b3f52b/tumblr_inline_p7a7k8r7cR1txw1p5_500.gif" alt="Subtle Animated Background" style="width: 100%; height: 180px; object-fit: cover; opacity: 0.05; position: absolute; top: 0; left: 0; z-index: -1; border-radius: 10px;">
</div>

---

<img src="https://raw.githubusercontent.com/AhmedAaliyan/AhmedAaliyan/main/assets/animated_divider_1.svg" alt="Animated Divider" class="section-divider">

## **🚀 My Core Expertise: Animated Skill Showcase**

<div align="center">
  <p style="color: var(--light-text-color);">Hover over the icons to unveil my mastery!</p>
  <div class="skill-grid" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); gap: 30px; margin-top: 40px;">

    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">React</p>
      <span class="tooltip-text">Building scalable SPAs with Hooks and Context API.</span>
    </div>
    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg" alt="Tailwind CSS" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">Tailwind CSS</p>
      <span class="tooltip-text">Rapid UI development with utility-first CSS.</span>
    </div>
    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" alt="TypeScript" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">TypeScript</p>
      <span class="tooltip-text">Enhancing code robustness and maintainability with static typing.</span>
    </div>
    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JavaScript" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">JavaScript</p>
      <span class="tooltip-text">Deep understanding of ES6+, async ops, and modern features.</span>
    </div>
    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">HTML5</p>
      <span class="tooltip-text">Semantic and accessible markup for modern web experiences.</span>
    </div>
    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">CSS3</p>
      <span class="tooltip-text">Styling mastery, including animations, flexbox, and grid.</span>
    </div>
    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://tanstack.com/build/_assets/query-dark-d017b203.svg" alt="TanStack Query" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">TanStack Query</p>
      <span class="tooltip-text">Efficient data fetching, caching, and state management.</span>
    </div>
    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg" alt="Firebase" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">Firebase</p>
      <span class="tooltip-text">Realtime databases, authentication, and hosting for full-stack solutions.</span>
    </div>
    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vercel/vercel-original.svg" alt="Vercel" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">Vercel</p>
      <span class="tooltip-text">Seamless deployment and hosting for front-end applications.</span>
    </div>
    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt="Git" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">Git</p>
      <span class="tooltip-text">Version control for collaborative and efficient development workflows.</span>
    </div>
    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" alt="GitHub" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">GitHub</p>
      <span class="tooltip-text">Collaboration, code hosting, and project management.</span>
    </div>
    <div class="skill-item" style="position: relative; display: inline-block;">
      <img src="https://www.svgrepo.com/show/354223/rest-api.svg" alt="REST API" width="80" height="80" class="animated-skill">
      <p style="margin-top: 10px; color: var(--text-color); font-weight: bold;">REST API</p>
      <span class="tooltip-text">Designing and consuming robust web services.</span>
    </div>
  </div>

  <h3 style="margin-top: 50px; color: var(--text-color);">Proficiency Snapshot:</h3>
  <img src="https://github.com/AhmedAaliyan/AhmedAaliyan/blob/main/assets/proficiency_bar.svg?raw=true" alt="Ahmed Aaliyan's Proficiency Bar" style="width: 80%; max-width: 700px; margin-top: 20px; border-radius: 8px; box-shadow: 0 4px 15px var(--shadow-light);">
  <p style="font-style: italic; color: var(--light-text-color); font-size: 0.9em;">(Data updated daily via GitHub Actions for dynamic progress)</p>
</div>

---

<img src="https://raw.githubusercontent.com/AhmedAaliyan/AhmedAaliyan/main/assets/animated_divider_2.svg" alt="Animated Divider" class="section-divider">

## **✨ Featured Projects: Visual & Engaging Showcase**

<div align="center">
  <p style="color: var(--light-text-color);">Experience my work in action!</p>
  <div class="project-carousel" style="display: flex; overflow-x: auto; scroll-snap-type: x mandatory; -webkit-overflow-scrolling: touch; gap: 30px; padding: 20px 0; max-width: 100%; margin: 20px auto; border-radius: 12px; background: var(--bg-light);">

    <div class="project-card card-style" style="flex: 0 0 350px; scroll-snap-align: start; transform: translateZ(0);">
      <img src="https://via.placeholder.com/350x200.gif?text=Project+Aurora+Demo" alt="Project Aurora Demo" style="width: 100%; height: 200px; object-fit: cover;">
      <div style="padding: 20px;">
        <h3 style="margin-top: 0; color: var(--text-color);">Project Aurora</h3>
        <p style="font-size: 0.9em; color: #555;">A dynamic e-commerce platform built with **React, Tailwind CSS, and TanStack Query**, integrating **Firebase** for backend services.</p>
        <div style="margin-top: 20px; display: flex; justify-content: space-around;">
          <a href="https://your-project-aurora-demo.vercel.app/" target="_blank" rel="noopener noreferrer" class="animated-button live-demo">Live Demo</a>
          <a href="https://github.com/AhmedAaliyan/project-aurora-repo" target="_blank" rel="noopener noreferrer" class="animated-button view-code">View Code</a>
        </div>
      </div>
    </div>

    <div class="project-card card-style" style="flex: 0 0 350px; scroll-snap-align: start; transform: translateZ(0);">
      <img src="https://via.placeholder.com/350x200.gif?text=Interactive+Portfolio+Demo" alt="Interactive Portfolio Demo" style="width: 100%; height: 200px; object-fit: cover;">
      <div style="padding: 20px;">
        <h3 style="margin-top: 0; color: var(--text-color);">My Personal Portfolio</h3>
        <p style="font-size: 0.9em; color: #555;">A cutting-edge, visually rich portfolio showcasing interactive experiences and animations, deployed with **Vercel**.</p>
        <div style="margin-top: 20px; display: flex; justify-content: space-around;">
          <a href="https://your-portfolio-demo.vercel.app/" target="_blank" rel="noopener noreferrer" class="animated-button live-demo">Live Demo</a>
          <a href="https://github.com/AhmedAaliyan/your-portfolio-repo" target="_blank" rel="noopener noreferrer" class="animated-button view-code">View Code</a>
        </div>
      </div>
    </div>

    <div class="project-card card-style" style="flex: 0 0 350px; scroll-snap-align: start; transform: translateZ(0);">
      <img src="https://via.placeholder.com/350x200.gif?text=SaaS+Dashboard+Demo" alt="SaaS Dashboard Demo" style="width: 100%; height: 200px; object-fit: cover;">
      <div style="padding: 20px;">
        <h3 style="margin-top: 0; color: var(--text-color);">SaaS Dashboard UI</h3>
        <p style="font-size: 0.9em; color: #555;">A complex SaaS dashboard with dynamic charts and real-time data visualization using **REST APIs** and **TypeScript**.</p>
        <div style="margin-top: 20px; display: flex; justify-content: space-around;">
          <a href="https://your-saas-dashboard-demo.vercel.app/" target="_blank" rel="noopener noreferrer" class="animated-button live-demo">Live Demo</a>
          <a href="https://github.com/AhmedAaliyan/saas-dashboard-repo" target="_blank" rel="noopener noreferrer" class="animated-button view-code">View Code</a>
        </div>
      </div>
    </div>

    </div>
</div>

---

<img src="https://raw.githubusercontent.com/AhmedAaliyan/AhmedAaliyan/main/assets/animated_divider_3.svg" alt="Animated Divider" class="section-divider">

## **📊 My GitHub Story: Dynamic Stats**

<div align="center">
  <p style="color: var(--light-text-color);">Beyond the numbers, see my impact!</p>

  <img src="https://github.com/AhmedAaliyan/AhmedAaliyan/blob/main/assets/animated_heatmap.svg?raw=true" alt="Ahmed Aaliyan's Animated GitHub Contribution Heatmap" style="width: 90%; max-width: 800px; margin-top: 30px; border-radius: 8px; box-shadow: 0 4px 15px var(--shadow-medium);">

  <div style="display: flex; justify-content: space-around; margin-top: 40px; flex-wrap: wrap; gap: 20px;">
    <div class="chart-container card-style" style="width: 300px; height: 300px; padding: 15px;">
      <img src="https://github.com/AhmedAaliyan/AhmedAaliyan/blob/main/assets/top_languages_chart.svg?raw=true" alt="Ahmed Aaliyan's Animated Top Languages Chart" style="width: 100%; height: calc(100% - 25px);">
      <p style="font-weight: bold; margin-top: 10px; color: var(--text-color);">Top Languages</p>
    </div>

    <div class="chart-container card-style" style="width: 300px; height: 300px; padding: 15px;">
      <img src="https://github.com/AhmedAaliyan/AhmedAaliyan/blob/main/assets/commit_streak.svg?raw=true" alt="Ahmed Aaliyan's Animated Commit Streak" style="width: 100%; height: calc(100% - 25px);">
      <p style="font-weight: bold; margin-top: 10px; color: var(--text-color);">Commit Streak</p>
    </div>
  </div>
  <p style="font-style: italic; color: var(--light-text-color); margin-top: 20px; font-size: 0.9em;">(Data fetched and rendered dynamically via GitHub Actions)</p>
</div>

---

<img src="https://raw.githubusercontent.com/AhmedAaliyan/AhmedAaliyan/main/assets/animated_divider_4.svg" alt="Animated Divider" class="section-divider">

## **💡 Currently & Learning: Real-time Insights**

<div align="center">
  <p style="color: var(--light-text-color);">What's on my dev radar right now!</p>

  <div style="display: flex; justify-content: space-around; flex-wrap: wrap; margin-top: 30px; gap: 20px;">
    <div class="dynamic-section card-style" style="padding: 25px; margin: 0; width: 48%;">
      <h3 style="margin-top: 0; color: var(--text-color);"><span style="margin-right: 10px;">⚡</span>Working On:</h3>
      <p class="latest-activity" style="font-size: 1.1em; color: #333; line-height: 1.5;">
        <span style="font-weight: bold;">_Fetching Latest Commit..._</span>
        </p>
    </div>

    <div class="dynamic-section card-style" style="padding: 25px; margin: 0; width: 48%;">
      <h3 style="margin-top: 0; color: var(--text-color);"><span style="margin-right: 10px;">📚</span>Currently Learning:</h3>
      <div style="display: flex; align-items: center; margin-bottom: 15px;">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg" alt="Next.js Icon" width="35" height="35" style="margin-right: 15px;">
        <span style="font-size: 1.1em; color: #333; font-weight: 500;">Next.js (SSR/SSG deep dive)</span>
        <img src="https://github.com/AhmedAaliyan/AhmedAaliyan/blob/main/assets/nextjs_progress.svg?raw=true" alt="Next.js Progress" style="width: 100px; height: 8px; margin-left: auto;">
      </div>
      <div style="display: flex; align-items: center; margin-bottom: 15px;">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/graphql/graphql-plain.svg" alt="GraphQL Icon" width="35" height="35" style="margin-right: 15px;">
        <span style="font-size: 1.1em; color: #333; font-weight: 500;">GraphQL</span>
        <img src="https://github.com/AhmedAaliyan/AhmedAaliyan/blob/main/assets/graphql_progress.svg?raw=true" alt="GraphQL Progress" style="width: 100px; height: 8px; margin-left: auto;">
      </div>
      </div>
  </div>

  <h3 style="margin-top: 50px; color: var(--text-color);"><span style="margin-right: 10px;">🎧</span>Vibin' To:</h3>
  <div class="spotify-now-playing card-style" style="display: flex; align-items: center; background: #282828; color: #fff; padding: 15px 25px; max-width: 450px; margin: 20px auto;">
    <img src="https://via.placeholder.com/80x80.png?text=Album+Art" alt="Album Art" style="width: 80px; height: 80px; border-radius: 8px; margin-right: 20px; object-fit: cover;">
    <div>
      <p style="font-size: 1.2em; margin: 0; font-weight: bold;">_Fetching Song Title..._</p>
      <p style="font-size: 1em; margin: 5px 0 0; color: #b3b3b3;">_Fetching Artist Name..._</p>
      <img src="https://github.com/AhmedAaliyan/AhmedAaliyan/blob/main/assets/spotify_progress.svg?raw=true" alt="Spotify Progress Bar" style="width: 100%; height: 5px; margin-top: 10px; border-radius: 3px;">
    </div>
  </div>
  <p style="font-style: italic; color: var(--light-text-color); font-size: 0.9em;">(Powered by Spotify API via GitHub Actions - updates every ~30 mins)</p>
</div>

---

<img src="https://raw.githubusercontent.com/AhmedAaliyan/AhmedAaliyan/main/assets/animated_divider_5.svg" alt="Animated Divider" class="section-divider">

## **✉️ Connect With Me: Animated & Engaging**

<div align="center">
  <p style="color: var(--light-text-color);">Let's build something amazing together!</p>
  <div class="social-icons" style="margin-top: 30px; display: flex; justify-content: center; gap: 30px;">
    <a href="https://linkedin.com/in/ahmedaaliyan" target="_blank" rel="noopener noreferrer">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" alt="LinkedIn" width="60" height="60" class="animated-social-icon">
    </a>
    <a href="https://twitter.com/ahmedaaliyan" target="_blank" rel="noopener noreferrer">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/twitter/twitter-original.svg" alt="Twitter" width="60" height="60" class="animated-social-icon">
    </a>
    <a href="mailto:your.email@example.com" target="_blank" rel="noopener noreferrer">
      <img src="https://upload.wikimedia.org/wikipedia/commons/4/4e/Mail_icon_%28grey%29.svg" alt="Email" width="60" height="60" class="animated-social-icon">
    </a>
    <a href="https://your-personal-website.com/contact" target="_blank" rel="noopener noreferrer" class="animated-contact-button">
      Get in Touch!
    </a>
  </div>
</div>

---

<img src="https://raw.githubusercontent.com/AhmedAaliyan/AhmedAaliyan/main/assets/animated_divider_6.svg" alt="Animated Divider" class="section-divider">

## **🎨 Creative Corner & Hidden Gems**

<div align="center">
  <h3 style="margin-top: 40px; color: var(--text-color);">🤫 Find the hidden gem...</h3>
  <p class="easter-egg" style="color: transparent; cursor: pointer; user-select: none; font-size: 0.8em; transition: color 0.5s ease-in-out;">
    &lt;!-- Psst! Did you know I also dabble in generative art? Hover me! --&gt;
    <span style="color: var(--secondary-color); font-weight: bold;">
      Check out my creative coding experiments <a href="https://your-generative-art-link.com" target="_blank" rel="noopener noreferrer" style="color: var(--primary-color); text-decoration: underline;">here!</a>
    </span>
    </p>

  <p style="font-style: italic; color: var(--light-text-color); margin-top: 30px; font-size: 0.85em;">(Built with passion, performance, and a keen eye for detail.)</p>
</div>
