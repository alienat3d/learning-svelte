<script>
  let name = 'Rich';
  let num = 37;
  let src = 'https://avatars.githubusercontent.com/u/1162160?v=4';
  let altText = 'Rich Harris photo';
	let htmlString = '<strong>This is bold text</strong> with <em>a little bit of italic</em>.';
</script>

<main>
  <h1>Hello {name}!</h1>
  <h2>{name.toUpperCase()}</h2>
  <h2>{(Math.random() * num).toFixed(3)}</h2>
  <img {src} alt={altText} />
	<p>{@html htmlString}</p>
  <!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->
</main>
<!-- Стили локализованы и не распространяются на другие компоненты. Если же требуется создать глобальные стили, то для этого у нас есть файл global.css, либо мы можем использовать специальный синтаксис :global() -->
<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  :global(h1) {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

	img {
		border-radius: 50%;
		width: 200px;
		height: auto;
	}

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
