<div id="leftBar">
    <div id="leftBar-top">
        <a href="/" class="transparentButton leftBarButton" on:click={() => changePressedButton("home")} id="leftBar-homeButton">Home</a>
        <a href="/accounts" class="transparentButton leftBarButton" on:click={() => changePressedButton("accounts")} id="leftBar-accountsButton">Accounts</a>
        <a href="/transactions" class="transparentButton leftBarButton" on:click={() => changePressedButton("transactions")} id="leftBar-transactionsButton">Transactions</a>
    </div>
    

    <a href="/user" class="transparentButton leftBarButton" on:click={() => changePressedButton("user")} id="leftBar-userButton"><svg id="leftBar-userButton-svg" data-slot="icon" aria-hidden="true" fill="none" stroke-width="1.5" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M17.982 18.725A7.488 7.488 0 0 0 12 15.75a7.488 7.488 0 0 0-5.982 2.975m11.963 0a9 9 0 1 0-11.963 0m11.963 0A8.966 8.966 0 0 1 12 21a8.966 8.966 0 0 1-5.982-2.275M15 9.75a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" stroke-linecap="round" stroke-linejoin="round"></path></svg> Username</a>
</div>

<script>

    function changePressedButton(id) {
        document.getElementById("leftBar-homeButton").style = "background-color: auto";
        document.getElementById("leftBar-accountsButton").style = "background-color: auto";
        document.getElementById("leftBar-transactionsButton").style = "background-color: auto";
        document.getElementById("leftBar-userButton").style = "background-color: auto";
        
        document.getElementById(`leftBar-${id}Button`).style = "background-color: rgb(235, 235, 235)";
    }
</script>

<style> 


    #leftBar {
        height: calc(100% - 1.4em);
        width: 10em;
        border-radius: 0.7em;
        border: none;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        gap: 1em;
        padding: 0.7em;
    }

    #leftBar-top {
        display: flex;
        flex-direction: column;
        gap: 1em;
    }

    #leftBar-userButton-svg {
        height: 2em;
    }

    #leftBar-userButton {
        display: flex;
        flex-direction: row;
        align-items: center;
        color: red;
    }

    .leftBarButton {
        width: 7.5em;
        font-size: large;
        text-align: start;
    }
</style>

<slot />