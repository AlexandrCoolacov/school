<template>
    <div class="headerNav">
        <a href="#" class="header-btn catalog">Каталог</a>
        <a href="#" class="header-btn activation">Активация</a>
        <a href="#" class="header-btn enter">Вход</a>
    </div>
</template>

<script>

export default {
    name: 'HeaderNav',
}
</script>

<style lang="scss" scoped>
.headerNav {
    grid-area: nav;
    display: grid;
    grid-template-columns: repeat(3, 145px );
    grid-template-rows: 43px;
    grid-gap: 8px;
    justify-content: center;

    a{
        display: grid;
        border-radius: 10px;
        /* width: 145px; */
        /* color: white; */
        text-decoration: none;
        
        box-sizing: border-box;
        font-size: 17.5px;
        font-weight: 300;
        letter-spacing: .03em;
        line-height: normal;
        white-space: nowrap;
        text-align: center;
        user-select: none;
        align-items: center;
        &.header-btn {
            background-color: #00C0FF;
            &:hover {background: linear-gradient(#00BBEB, #004fe5) ;}
                
        }
    
}
    
}


@media (max-width:950px) {
  .headerNav{
    grid-area: nav;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows:  repeat(3 , 43px);
    grid-gap: 8px;
    justify-content: center;
    a{
        width: 100%;
    }
  } 
}

    
</style>