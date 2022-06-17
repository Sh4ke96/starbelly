<template>
  <nav class="headerNav">
    <ul class="headerNav__list">
      <li class="header__navItem">
        <a href="/" class="header__navLink">About</a>
      </li>
      <li class="header__navItem">
        <a href="/" class="header__navLink">Menu</a>
      </li>
      <li class="header__navItem">
        <a href="/" class="header__navLink">Shop</a>
      </li>
      <li class="header__navItem">
        <a href="/" class="header__navLink">Blog</a>
      </li>
      <li class="header__navItem">
        <a href="/" class="header__navLink">Gallery</a>
      </li>
      <li class="header__navItem">
        <a href="/" class="header__navLink">Contact</a>
      </li>
    </ul>
  </nav>
  <div class="headerNav__icons">
    <ul>
      <li class="li__icons">
        <button id="bagIcon" class="bagIcon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-bag"
            viewBox="0 0 16 16"
          >
            <path
              d="M8 1a2.5 2.5 0 0 1 2.5 2.5V4h-5v-.5A2.5 2.5 0 0 1 8 1zm3.5 3v-.5a3.5 3.5 0 1 0-7 0V4H1v10a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2V4h-3.5zM2 5h12v9a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V5z"
            />
          </svg>
          <i class="bagIcon-number">5</i>
        </button>
      </li>
      <li class="li__icons">
        <button id="dotIcon" class="dotIcon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="16"
            fill="currentColor"
            class="bi bi-three-dots-vertical"
            viewBox="0 0 16 16"
          >
            <path
              d="M9.5 13a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0z"
            />
          </svg>
        </button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.headerNav {
  &__list {
    display: flex;
    list-style: none;
    margin: 0;
  }
  .header__navItem {
    padding: 0 3rem;
  }
  .header__navLink {
    color: var(--secondary);
    text-decoration: none;
    font-size: 1.7rem;
    font-weight: 400;
    transition: 0.3s ease-in-out;
  }
  .header__navLink:hover {
    color: var(--primary);
  }
}

.headerNav__icons {
  ul {
    display: flex;
    align-items: center;
    list-style: none;
    margin: 0;
    .li__icons {
      button {
        background-color: transparent;
        outline: none;
        border: none;
        cursor: pointer;
      }
      .bagIcon {
        background-color: var(--lightGray);
        box-shadow: 0 0 0 2px #ffffff;
        border-radius: 50%;
        display: inline-flex;
        justify-content: center;
        align-items: center;
        position: relative;
        padding: 0 !important;
        margin: 0;
        width: 6rem;
        height: 6rem;
      }
      .bagIcon:hover {
        background-color:#f5f6fa;
        transition: 0.3s ease-in-out;
      }
      .dotIcon {
        padding-left: 2rem;
      }
      .bagIcon-number {
        font-style: normal;
        font-weight: 500;
        font-size: 1.2rem;
        position: absolute;
        top: 0;
        right: 0;
        text-align: center;
        line-height: 2rem;
        background-color: var(--primary);
        border-radius: 1.5rem;
        height: 2rem;
        padding: 0 0.6rem;
        box-shadow: 0 0.1rem 0.5rem 0 rgba(0, 0, 0, 0.1);
      }
    }
    .bi-bag,
    .bi-three-dots-vertical {
      width: 2.5rem;
      height: 2.5rem;
    }
  }
}
</style>