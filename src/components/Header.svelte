<script>
  let navItems = [{ title: "GPU" }, { title: "CPU" }, { title: "CONSOLE" }];
</script>

<header>
  <div>
    <h1>Silifind</h1>
    <nav>
      <ul>
        {#each navItems as { title }, i}
          <li>{title}</li>
        {/each}
      </ul>
    </nav>
  </div>
</header>

<style>
  header {
    background-image: linear-gradient(
      180deg,
      rgba(0, 0, 0, 0.65) 3%,
      rgba(0, 0, 0, 0) 100%
    );
    font-family: "poppins", Arial, Helvetica, sans-serif;
    width: 100%;
    height: 64px;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
  }

  div {
    height: 64px;
    width: min(100%, 1080px);
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: auto;
  }

  h1 {
    text-transform: uppercase;
    font-weight: 400;
    font-size: 36px;
  }

  ul {
    list-style: none;
    display: flex;
  }

  li {
    margin-right: 30px;
    text-transform: uppercase;
    font-weight: 500;
    font-size: 18px;

    cursor: pointer;
    transition: color 0.2s 0s ease;
  }

  li:hover {
    color: var(--header-secondary);
  }
</style>
