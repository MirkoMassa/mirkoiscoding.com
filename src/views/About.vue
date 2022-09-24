<template>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@500&display=swap" rel="stylesheet">
    <nav>    
        <a href="/" style="text-decoration:none;" id = "icon"></a>

        <ul id = "nav-div">
            <a href="/" class = "nav-button" style="text-decoration:none;">home</a>
            <a href="/about" class = "nav-button" style="text-decoration:none;">about</a>
            <a href="" class = "nav-button" style="text-decoration:none;">cv</a>
        </ul>

        <div id="socials-div">
            <a href="https://github.com/MirkoMassa" id = "gh" class = "nav-social"></a>
            <a href="https://www.instagram.com/mirko__sl/" id = "ig" class = "nav-social"></a>
            <a href="https://www.linkedin.com/in/mirko-massa" id = "ln" class = "nav-social"></a>
            <a href="https://t.me/mirkez" id = "tg" class = "nav-social"></a>
        </div>
    </nav>
    <div id="ab-container">

        <h1>About me...</h1>
        <h2>Hi! I’m Mirko, a 21 years old developer from Italy, 
            mainly focused on back-end web developement, 
            but hungry to earn experience and learn a lot more about this universe.
            When I’m not squeezing my brain over poorly written code, I practice strength training, 
            read mangas and ride around with my OneWheel. I also love hitting the touge with a nice RWD car!

            This website is built with Vue.js. You can check my other projects on GitHub!</h2>
        <div id="separator"></div>
        <h1>Contacts</h1>
        <h3>mirkomassa18@gmail.com</h3>
        <h3>+39 346 945 0170</h3>

    </div>
        

</template>
<script>
export default {
    
}
</script>
<style>
    #ab-container{
        opacity: 0;
        display: flex;
        flex-direction: column;
        align-items: left;
        justify-content: left;
    }
    h1{
        padding-left: 20px;
        padding-top: 30px;
        margin: 0;
        font-family: 'Roboto', sans-serif;
        white-space: nowrap;
        font-style: normal;
        font-weight: 800;
        font-size: 70px;
        line-height: 50px;
        text-align: left;
        letter-spacing: -1.5px;
        color: #263238;
    }
    h2{
        padding-left: 20px;
        padding-right: 20px;
        padding-top: 20px;
        margin: 0;
        font-family: 'Roboto' ,serif;
        font-style: normal;
        text-align: left;
        font-weight: lighter;
        font-size: 30px;
    }
    h3{
        padding-left: 20px;
        padding-right: 20px;
        padding-top: 20px;
        margin: 0;
        font-family: 'Roboto' ,serif;
        font-style: normal;
        text-align: left;
        font-weight: lighter;
        font-size: 25px;
    }
    #separator{
        margin-top: 20px;
        border: 0.5px solid #263238;
    }
</style>