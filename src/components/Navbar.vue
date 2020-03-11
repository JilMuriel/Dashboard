<template>
    <nav>
        <section class="top-nav">
            <div class="burger">
                <img src="../assets/img/bars-icon.png" alt="">
            </div>
            <div class="logo-container__primary">
                <span class="icon">Kollab</span>
            </div>
            <div class="link-block">
                <a href="#" class="user-block">
                    <img class="user-block__icon" src="../assets/img/user-icon.png" alt="user-icon" >
                    {{ userData.username }}      
                </a>
                <a href="#">
                    Bell
                </a>
                <a>Message</a>
            </div>
        </section>
        <div class="main-top">
            <div class="logo-container__secondary">
                <img src="../assets/img/analytics-icon.png" alt="">
                <span>Analytics</span>
            </div>
        </div>
    </nav>
</template>
<script>
export default {
    data: () => {
       return {
           userData: 
               {
                   id: '12345678',
                   username: 'Katrina',
               }
       }
    },
}
</script>
<style lang="scss" scoped>
    .icon {
        font-family: 'Poppins', sans-serif;
        font-weight: bolder;
        font-size: 1.2em;
        color: hsl(150, 1%, 39%);
    }
    nav {
        border: 1px solid black;
        background: #fff;
    }
    .top-nav {
        padding: 0 30px;
        display: flex;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        border: 1px solid black;
        min-height: 55px;
        align-items: center;
        div {
            border: 1px solid black;
        }
    }
    .main-top {
        min-height: 60px;
        padding: 0 30px;
        border: 1px solid black;
        align-items: center;
        display: flex;
    }
    .link-block {
        display: flex;
        margin-left: auto;
        align-items: center;
        justify-content: flex-endd;
        font-size: 0.8em;
        a {
            font-size: inherit;
            font-weight: bold;
            margin-left: 30px;
        }
    }
    .user-block {
        display: flex;
        align-items: center;
        font-weight: bold;
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

</style>