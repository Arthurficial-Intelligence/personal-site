<script>
    import headshot from "../assets/img/headshot.png";
</script>

<div class="home-page-container">
    <p class="opener">
        Welcome! My name is <span class="name"><a href="/about">Arthur</a></span
        >
        <br />
        I am fasinated with Human-Computer Interaction
    </p>
</div>

<style>
    .home-page-container {
        height: 60vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    img {
        border-radius: 150px;
        margin-right: 10px;
    }

    .opener {
        padding-top: 10px;
        font-size: 32px;
        line-height: 40px;
    }
    a {
        text-decoration: none;
        color: orange;
    }
    .name {
        font-size: 32px;
        padding-left: 7px;
        transition: all 0.5s;
    }
    .name:hover {
        font-size: 40px;
        margin-left: 0px;
    }
</style>
