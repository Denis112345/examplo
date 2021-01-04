<template>
  <div class="wrapper">
    <div class="HeaderSerch">
      <img class="HeaderSerch__logo" src="@/img/LOGO.png" alt="" />

      <div class="HeaderSerch__menu">
        <nav class="nav">
          <input class="nav__check" type="checkbox" id="showmenu" />
          <label class="nav__showmenu" for="showmenu">&#9776;</label>
          <label class="nav__back" for="showmenu"></label>

          <ul class="burger__menu">
            <li><a class="burger__item" href="#">Catalog</a></li>
            <li>
              <a class="burger__item" href="#">About</a>
            </li>
            <li><a class="burger__item" href="#">Price</a></li>
            <li><a class="burger__item" href="#">Contacts</a></li>
            <li><a class="burger__item" href="#">Other</a></li>
          </ul>
        </nav>
        В каталог
      </div>

      <input class="HeaderSerch__search" />
      <button class="search___Submit" type="submit">
        <img src="@/img/SearchImg.png" alt="" />
      </button>

      <div class="HeaderSerch__icons">
        <a href="#" class="icons__enterIcon">
          <div class="enterIcon__content">
            <img src="@/img/enterIcon.png" alt="enerIcon" />
            Войти
          </div>
        </a>
        <a href="#" class="icons__basketIcon">
          <div class="basketIcon__content">
            <img src="@/img/basketIcon.png" alt="basketIcon" />
            Корзина
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.wrapper {
  display: flex;
}

.HeaderSerch {
  display: flex;
  margin: 0 auto;

  min-width: 1200px;
}

.HeaderSerch__menu {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0.75% 2.5%;
  border-radius: 10px;
  color: white;
  white-space: nowrap;

  margin-right: 2.2%;

  background: #10b648;
}

nav > input {
  display: none;
}
.nav__showmenu {
  position: relative;
  z-index: 3;

  margin-right: 9px;

  cursor: pointer;

  font-size: 18px;
}

.burger__menu {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  list-style: none;
  padding: 0;
  color: #fff;
  overflow: hidden;
  width: 15%;
  margin: 0;
  padding: 50px 0 10px 0;
  height: 150px;
  text-transform: uppercase;
  line-height: 2em;
  background-color: #2c2c2c;

  transform: translateX(-100%);
  transition: transform 0.3s;
  will-change: transform;
}

.burger__item {
  display: inline-block;

  text-decoration: none;
  color: #fff;
}

.nav__check:checked ~ .burger__menu {
  transform: translateX(0);
}

.HeaderSerch__logo {
  margin-right: 2.2%;
  align-self: center;
}

.HeaderSerch__search {
  height: 3.5em;
  width: 51.2%;

  border: 1px solid #ebebeb;

  border-radius: 10px;
  border-top-right-radius: 0px;
  border-bottom-right-radius: 0px;
  border-right: none;
}

.search___Submit {
  position: relative;
  right: 0.4%;

  background: #10b648;
  border: 0px;
  height: 3.8em;
  width: 3.8em;

  margin-right: 6.1%;

  border-radius: 10px;
}

.HeaderSerch__icons {
  display: flex;

  align-items: center;

  color: #838282;
  font-weight: 600;
  font-size: 600;
  line-height: 19px;
  text-align: center;
}

.incons__enterIcon,
.incons__basketIcon {
  display: table;
  flex-direction: column;
  align-self: center;
}

.basketIcon__content,
.enterIcon__content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.icons__enterIcon {
  margin-right: 30px;
}

@media (max-width: 1200px) {
  .header {
    max-width: 917px;
  }
  .HeaderSerch {
    max-width: 917px;
  }
  .Header__serch {
    width: 41%;
  }
}

@media (max-width: 917px) {
  .HeaderSerch {
    min-width: 802px;
  }
  .Header__serch {
    width: 20rem;
  }
}
</style>
