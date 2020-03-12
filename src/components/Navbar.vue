<template>
  <nav>
    <section class="top-nav">
      <div class="burger">
        <img src="@/assets/img/bars-icon.png" />
      </div>
      <div class="logo-container__primary">
        <span class="icon">Kollab</span>
      </div>
      <div class="link-block">
        <section>
          <div class="dropdown">
            <a href="#" class="user-block link-hover">
              <img
                class="user-block__icon"
                src="@/assets/img/user-icon.png"
                alt="user-icon"
              />
              {{ userData.username }}
              <img
                class="arrow-down-icon"
                src="@/assets/img/arrow-down-icon.png"
              />
            </a>
            <div class="dropdown-content">
              <a href="#">Link 1</a>
            </div>
          </div>
        </section>
        <span class="line-breaker">|</span>
        <a href="#" class="user-block notif link-hover">
          <img class="bell-icon" src="@/assets/img/bell-icon.png" />
        </a>
        <span class="line-breaker">|</span>
        <a class="link-hover">
          <img class="help-icon" src="@/assets/img/help-icon.png" />
        </a>
      </div>
    </section>
    <div class="main-top">
      <div class="logo-container__secondary">
        <img src="../assets/img/analytics-icon.png" />
        <span>Analytics</span>
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  data: () => {
    return {
      userData: {
        id: "12345678",
        username: "Katrina"
      }
    };
  },
  methods: {
    methodToRunOnSelect(payload) {
      this.object = payload;
    }
  }
};
</script>
<style lang="scss" scoped>
nav {
    position: fixed;
    width: 100%;
    z-index: 10000;
      box-shadow: 0 1px 3px rgba(105, 105, 105, 0.12)
}
.burger {
  img {
    max-height: 13px;
    cursor: pointer;
    width: auto;
  }
}
.notif {
  position: relative;
  left: 6px;
  &:after {
    padding: 1px 4px;
    position: relative;
    bottom: 7px;
    left: -8px;
    content: "2";
    font-size: 0.7em;
    background: #fa8923;
    color: #fff;
    font-weight: bold;
  }
}
.bell-icon {
  max-height: 22px;
}

.help-icon {
  max-height: 22px;
}
.arrow-down-icon {
  margin-left: 10px;
  max-height: 7px;
  widows: auto;
}
.icon {
  font-family: "Poppins", sans-serif;
  font-weight: bolder;
  font-size: 1.2em;
  color: hsl(150, 1%, 39%);
}
nav {
  background: #fff;
}
.top-nav {
  padding: 0 30px;
  display: flex;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  min-height: 55px;
  align-items: center;
}
.main-top {
  min-height: 60px;
  padding: 0 30px;
  align-items: center;
  display: flex;
}
.link-block {
  display: flex;
  margin-left: auto;
  align-items: center;
  justify-content: flex-endd;
  a {
    font-size: inherit;
    font-weight: 600;
    font-size: 0.8em;
    text-decoration: none;
    color: #707070;
  }
  @media only screen and (max-width: 426px) {
    display: none;
  }
}
.user-block {
  display: flex;
  align-items: center;
  font-weight: bold;
}
.link-hover {
  opacity: 0.8;
  transition: ease-in-out;
  &:hover {
    opacity: 1;
  }
}
.user-block__icon {
  max-height: 25px;
  width: auto;
  margin-right: 10px;
}
.logo-container__primary {
  text-align: center;
}
.logo-container__secondary {
  display: flex;
  align-items: center;
  font-weight: bold;
  font-size: 1.3em;
  img {
    margin-right: 10px;
    max-height: 23px;
    width: auto;
  }
}
ul {
  // display: flex;
  // justify-content: flex-end;
  // align-items: center;
  margin: 0;
  li {
    font-size: 0.9em;
    color: #434343;
    list-style: none;
    margin-left: 30px;
  }
}
.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  min-width: 130px;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  padding: 12px 20px;
  text-align: right;
  font-size: 0.9em;
  left: -60px;
  z-index: 1000;
  border-radius: 2px;
  a {
    &:hover {
      color: blue;
    }
  }
}

.dropdown:hover .dropdown-content {
  display: block;
}
.line-breaker {
    color: #E5E5E5;
    margin: 0 10px
}
</style>
