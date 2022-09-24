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
        <div id="hamburger"></div>

    </nav>

    <div id="rect-container"
        @mouseover ="transitionmouseover('#rect2')"
        @mouseleave ="transitionmouseleave('#rect2')">
        <div id = "rect">
            <div id = "name">Mirko Massa</div>
            <div id = "webdev">web dev.</div>
        </div>
        <div id = "rect2"></div>
        
    </div>
</template>
<script>
import { gsap } from 'gsap';
import CSSRulePlugin from "gsap/CSSRulePlugin";
gsap.registerPlugin(CSSRulePlugin);



export default {
    data() {
        return {
            
        }
    },
    methods: {
        transitionmouseover(element){
                gsap.to(element, 
                {
                    margin: '0',
                    opacity: 0.5,
                    duration: 0.7,
                    ease: gsap.easeInOut
                })
                gsap.to(element, 
                {
                    margin: '0',
                    opacity: 0.5,
                    duration: 0.7,
                    ease: gsap.easeInOut
                })
        },
        transitionmouseleave(element){
                gsap.to(element, 
                {
                    margin: '0, 0, 20px, 220vw',
                    opacity: 0,
                    duration: 0.7,
                    ease: gsap.easeInOut
                })
        },
    },
}
</script>
<style>
    #rect-container{
        position: absolute;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-start;
        padding-top: 6vw;
        width: 100%;
        height: 710px;
        overflow: hidden;
        
    }
    #rect{
        opacity: 0;
        z-index: -1;
        align-self: center;


        display: flex;
        align-items: center;
        justify-content: center;

        width: 110%;
        height: 300px;
        
        transform: matrix(1, 0.10, -0.1, 1, 0, 0);
        background: #D9D9D9;
        box-shadow: inset 0px 4px 4px rgba(0, 0, 0, 0.1);
    }
    #rect2{

        z-index: -2;
        position: relative;
        z-index: 2;
        align-self: center;

        opacity: 0;
        margin-top: 20px;
        margin-left: 220vw;

        display: flex;
        align-items: center;
        justify-content: center;
        
        width: 110%;
        height: 300px;
        
        background: url(D:\Coding\personal-website\src\assets\post.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;

        transform: matrix(1, 0.10, -0.1, 1, 0, 0);
        box-shadow: inset 0px 4px 4px rgba(0, 0, 0, 0.1);
    }
    
    #name{
        position: absolute;
        width: auto;
        height: auto;
        z-index: 1;

        font-family: 'Roboto', sans-serif;
        white-space: nowrap;
        font-style: normal;
        font-weight: 800;
        font-size: 100px;
        line-height: 50px;
        text-align: center;
        letter-spacing: -1.5px;
        color: #263238;

        transform: matrix(1, -0.10, 0.1, 1, 0, 0);

    }
    #webdev{
        position: fixed;
        width: auto;
        height: auto;
        z-index: 1;
        top: 65%;
        left: 50%;
        

        text-align: center;
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 100;
        font-size: 30px;
        line-height: 20px;
        color: #000000;

        transform: matrix(1, -0.10, 0.1, 1, 0, 0);
    }

    @media all and (max-width: 400px){

        #name{
            font-size: 60px;
        }
        #webdev{
            font-size: 20px;   
            top: 60%;
            left: 50%;
        }
        #rect{
            height: 200px;
        }
    }
</style>