<script>
    import img from './img_path.json';
    // import Card from './components/Card.vue';
    
    export default {
        data(){
            return {
                images: img
            };
        }
    };
</script>

<template>
    <header>
        <div class="title">My Foto Koleksi Gw</div>
        <nav>
            <ul>
                <li id="nav-1">nav 1</li>
                <li id="nav-2">nav 2</li>
                <li id="nav-3">nav 3</li>
                <li id="nav-4">nav 4</li>
                <li id="nav-5">nav 5</li>
                <li id="nav-6">nav 6</li>
            </ul>
        </nav>
    </header>
    <main>
        <div class="container">
            <!-- <Card v-for="image in images" :key="image.id"  ></Card> -->
            <div class="card" v-for="image in images" :key="image.id">
                <img :src="image.path" :alt="image.title">
                <h2>{{ image.title }}</h2>
                <p>{{ image.description }}</p>
            </div>
            
        </div>
    </main>
    <footer>
        <p>Copyright@ Aji Pratama</p>
    </footer>
</template>

<style>
:root {
  --text: #6b6375;
  --text-h: #08060d;
  --bg: #fff;
  --border: #e5e4e7;
  --code-bg: #f4f3ec;
  --accent: #aa3bff;
  --accent-bg: rgba(170, 59, 255, 0.1);
  --accent-border: rgba(170, 59, 255, 0.5);
  --social-bg: rgba(244, 243, 236, 0.5);
  --shadow:
    rgba(0, 0, 0, 0.1) 0 10px 15px -3px, rgba(0, 0, 0, 0.05) 0 4px 6px -2px;

  --sans: system-ui, 'Segoe UI', Roboto, sans-serif;
  --heading: system-ui, 'Segoe UI', Roboto, sans-serif;
  --mono: ui-monospace, Consolas, monospace;

  font: 18px/145% var(--sans);
  letter-spacing: 0.18px;
  color-scheme: light dark;
  color: var(--text);
  background: var(--bg);
  text-align: center;
  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  @media (max-width: 1024px) {
    font-size: 16px;
  }
}

@media (prefers-color-scheme: dark) {
  :root {
    --text: #9ca3af;
    --text-h: #f3f4f6;
    --bg: #16171d;
    --border: #2e303a;
    --code-bg: #1f2028;
    --accent: #c084fc;
    --accent-bg: rgba(192, 132, 252, 0.15);
    --accent-border: rgba(192, 132, 252, 0.5);
    --social-bg: rgba(47, 48, 58, 0.5);
    --shadow:
      rgba(0, 0, 0, 0.4) 0 10px 15px -3px, rgba(0, 0, 0, 0.25) 0 4px 6px -2px;
  }

  #social .button-icon {
    filter: invert(1) brightness(2);
  }
}

#root {
  max-width: 100%;
  margin: 0 auto;
  text-align: center;
  border-inline: 1px solid var(--border);
  min-height: 100svh;
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
  /* padding: 2em; */
  gap: 2em;
}

body {
    margin: 0;
}

h1,
h2 {
  font-family: var(--heading);
  font-weight: 500;
  color: var(--text-h);
}

h1 {
  font-size: 56px;
  letter-spacing: -1.68px;
  margin: 32px 0;

  @media (max-width: 1024px) {
    font-size: 36px;
    margin: 20px 0;
  }
}

h2 {
  font-size: 24px;
  line-height: 118%;
  letter-spacing: -0.24px;
  margin: 0 0 8px;

  @media (max-width: 1024px) {
    font-size: 20px;
  }
}

p {
  margin: 0;
}

.card {
  border: var(--border) solid 2px;
  border-radius: 1em;
}

nav {
  background-color: var(--border);
}

nav ul {
  display: flex;
  justify-content: space-between;
  list-style: none;
  padding: 8px 4em;
}

.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2em;
  padding: 0 2em;
}


.title {
  margin: 0 2em;
}
</style>