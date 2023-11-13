<script>
    let toggle;
    let darkmode;

    function toggle_dark(){
        window.document.body.classList.toggle("dark-mode");
        
    }
</script>
<button on:click={toggle_dark} id="toggle">
    <i class="indicator"></i>
</button>

<style>
    #toggle {
        position: relative ;
        display: block;
        width: 80px;
        height: 40px;
        border-radius: 40px;
        background: #222;
        cursor: pointer;
        box-shadow: 0 8px 60px rgba(0,0,0,0.1),
                    inset 0 8px 8px rgba(0,0,0,0.1),
                    inset 0 -4px 4px rgba(0,0,0,0.1);
    }
    #toggle .indicator {
        position: absolute;
        top: 0;
        left: 0;
        width: 40px;
        height: 40px;
        background: linear-gradient(to bottom, #444, #222);
        border-radius: 50%;
        transform: scale(0.9);
        box-shadow: 0 8px 40px rgba(0,0,0,0.5),
                    inset 0 4px 4px rgba(255,255,255,0.2),
                    inset 0 4px 4px rgba(0,0,0,0.1);
        transition: 0.5s;
    }

    #toggle::after
</style>


<!-- 
<script>
    function toggle_dark(){
        window.document.body.classList.toggle.("dark-mode");
    }
</script>


<div class="toggle">
    <h2>Dark Mode</h2>
    <label for="dark"></label>
    <input type="checkbox" id="dark" />
</div>


<style>
    .toggle {
        display: grid;
        /* grid 2 columns, 1 row*/
        grid-template-columns: 1fr 1fr;
        align-items:center;
            
    }
    h2{
        /*Item should be in the first column at the start of cell*/
        grid-column: 1;
        color: #B2B2B2;
        font-size: 18px;
    }
    label {
        /*Item should be in the second column at the end of cell*/
        /* It should also be centralized vertically*/
        align-self: center;
        grid-column: 2;
        justify-self: end;
        width: 60px;
        height: 31px;
        position: relative;
        display: block;
        background-color: aqua;
        border-radius: 40px;
        box-shadow: inset 0px 5px 15px rgba(0,0,0,0.4), inset 0px -5px 15px rgba(255,255,255,0.4);
        cursor: pointer;
    }
    label:after {
        content: "";
        width: 27px;
        height: 27px;
        position: absolute;
        top:2px;
        left:2px;
        background: red;
        border-radius: 40px;
    }

    input {
        width: 0;
        height: 0;
        visibility: hidden;
    }

    input:checked + label {
        background-color: aqua;
        box-shadow: inset 0px 5px 15px rgba(0,0,0,0.4), inset 0px -5px 15px rgba(255,255,255,0.4);

    }
    input:checked + label:after {
        left: 31px;
    }


</style> -->