<script>
  import DropdownItem from "./DropdownItem.svelte";

  export let navItems = [];

  let openedDropdown = "GPU";

  const handleMouseOver = title => {
    openedDropdown = title;
  };

  const handleMouseOut = () => {
    openedDropdown = null;
  };
</script>

<nav>
  <ul>
    {#each navItems as { title }, i}
      <li>
        <a
          href="#"
          on:mouseover={handleMouseOver(title)}
          on:mouseout={handleMouseOut}>{title}</a
        >
        <DropdownItem
          on:mouseover={handleMouseOver(title)}
          on:mouseout={handleMouseOut}
          {title}
          {openedDropdown}
        />
      </li>
    {/each}
  </ul>
</nav>

<style>
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
    position: relative;
  }
  a {
    text-transform: uppercase;
    font-weight: 500;
    font-size: 18px;
    transition: color 0.2s 0s ease;
    color: var(--header-primary);
    text-decoration: none;
  }
  a:hover {
    color: var(--header-secondary);
  }
</style>
