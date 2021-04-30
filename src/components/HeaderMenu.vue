
<template>
    <nav class='headerMenuWrapper'>
        <div 
        class="headerMenuBurger" 
        v-on:click = "changeBurgerClass =!changeBurgerClass"
        
        
        >

            <span></span>
            
        </div>
        <div 
        class="headerMenuList " 
        :class="{ active: changeBurgerClass }">
                <ul>
                    <li>
                        <a href="/pages/about">О проекте</a>
                    </li>
                    <li>
                        <a href="/news">Новости</a>
                    </li>
                    <li>
                        <a href="/feedback">Помощь</a>
                    </li>
                    <li>
                        <a href="/pages/apps">Скачать</a>
                    </li>
                </ul>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'HeaderMenu',
    data() {
        return {
            changeBurgerClass : true
        }
       
    }
    /* methods: {
        changeBurgerClass() {
            console.log('Hello');
            const headerMenuList = document.querySelectorAll('.headerMenuList')
            console.log(headerMenuList);
            headerMenuList.classList.toggle('active')

        }
    } */
}
</script>


<style lang="scss" scoped>
.headerMenuWrapper {
    grid-area: menu;
    top: 68px;
    position: relative;
    // top: 17px;
    display: grid;
    grid-template-columns: 25px 130px;
    grid-template-rows: 1fr;
    grid-gap: 20px;
    

    .headerMenuBurger {
    
        text-align: center;
        vertical-align: middle;
        justify-content: center;
        width: 35px;
        height: 24px;
        position: relative;

            span {
                position: absolute;
                top: 0px;
                width: 100%;  
                height: 4px;
                right: 0;
                background-color: #00c1ff;
                &:before {
                    content: "";
                    position: absolute;
                    width: 100%;
                    height: 4px;
                    top: 10px;
                    background-color: #00c1ff;
                    left: 0px;
                }
                &:after {
                    content: "";
                    position: absolute;
                    width: 100%;
                    height: 4px;
                    top: 20px;
                    background-color: #00c1ff;
                    left: 0px;
                }
            }
    
    
}

    .headerMenuList {

        display: grid;
        
        transition-duration: 1s;
        position: relative;
         overflow: hidden;
        max-width: 130px;
        max-height: 200px;
        border: 1.75px;
        padding: 6px;
        box-sizing: border-box;
        margin: 0;
        border-top: 2px solid #00C1FF;
        text-align: center;
        top: 12px;
        
        

            ul {
                display: grid;
                position: relative;
                
                text-align: start;
               transition-duration: 1s;
            transition-delay: 1s;
                
                padding: 0px;
                white-space: nowrap;
                margin: 0;
                
                box-sizing: border-box;
                overflow: hidden;
            /*  
                /* height: 0; */
                background-color: #fff;
                
                text-decoration: none;
                list-style-type: none;
                /* text-align: center; */
                    li {
                        max-width: 130px;
                        height: 36px;
                        a{
                            padding: 0 10px;
                            max-width: 130px;
                        text-decoration: none;
                        color: #575756;
                        &:hover {
                            text-decoration: underline;
                            }
                        }
                    }
                    
                }
        }
    
}

.active {
        display: grid;
        position: relative;
        opacity: 0; 
        transform: translate(-150px,0px);
        transition-duration: 1s;
        
        width: 100%; 
        z-index: -1;
        overflow: hidden;
        ul{
            transition-duration: 1s;
            transition-delay: 1s;
            transform: translate(0px,-200px);
        }
        
    }

@media (max-width:475px) {
  .headerMenuWrapper{
    grid-area: menu;
    top: 0px;
   border-top: 2px solid #00C1FF;
    display: grid;
    grid-template-columns:  1fr;
    grid-template-rows: 1fr;
    grid-gap: 20px;
    text-align: center;
    align-items: center;
    justify-content: center;

        .headerMenuBurger {
            display: none;
        }
        
        .headerMenuList {
        position: relative;
         margin: 0 auto;
        max-height: 200px;
        border: 1.75px;
        padding: 6px;
        box-sizing: border-box;
        margin: 0;
        opacity: 1; 
        width: 100%;
        text-align: center;
        top: 12px;
  }
    
  } 
  
  
}

</style>

