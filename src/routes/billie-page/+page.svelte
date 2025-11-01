<script>
	
    function playsound1() {
        new Audio("lovely.mp3").play();
    }
    function playsound2() {
        new Audio("birds of  feather.mp3").play();
    }
    function playsound3() {
        new Audio("bad guy.mp3").play();
    }
    function playsound4() {
        new Audio("when the partys over.mp3").play();
    }
    function playsound5() {
        new Audio("everything i wanted.mp3").play();
    }
    function playsound6() {
        new Audio("ocean eyes.mp3").play();
    }
    function playsound7() {
        new Audio("happier than ever.mp3").play();
    }
    function playsound8() {
        new Audio("wildflower.mp3").play();
    }
    function playsound9() {
        new Audio("what was i made for.mp3").play();
    }
    function playsound10() {
        new Audio("idontwannabeuanymore.mp3").play();
    }
    let albums = [
        {name: "Happier Than Ever", votes: 0},
        {name:"When We All Fall Asleep,Where Do We Go?", votes:0},
        {name:"Don't Smile At Me", votes:0},
        {name:"other", votes:0},
    ];
     function vote(album) {
    album.votes++;
    albums = [...albums];
  }
    $: totalvotes = albums.reduce((sum, a) => sum+a.votes, 0);
    let comment = "";
    let comments = [];
    function addcomment() {
        if (comment !== "") {
            comments.push(comment);
            comment = "";
        }
    }
</script>
<main>
    <h1 class="site-title"> Billie Eilish fanpage</h1>
    <div class="billie">
I started listening to Billie in 2019 even though I was only seven. People sometimes hated me for it or loved me, in 2021 
I mostly got hate because they taught she was a satanist. Even after that I still listened to her when I got hste, but 
I didn't purposely say it out loud that I really liked her music. <br> It was kinda weird seeing everyone fanning over her in 2024
because of her new album I'm not saying that I wasn't happy for her or anything but yk. <br> I really wanted to go to her concert 
whilw she was in europe but there was never a good time, I still really want to go maybe someday I will get a chance to go. <br>
My fav albums from her are hte(Happier than ever), wwafawdwg(when we all fall asleep where do we go), dsam (dont smile at me), hmhas
(hit me hard and soft) tbh I like almost every album she has ever released lol. <br> Here are some of my fav songs from her:ilomilo, xanny, 
goodbye, happier than ever,  Billie Bossa nova, There for I am, No time to die, GOLDWING, Getting Older, wish u were gay, my strange addiction,
listen before I go, I love u, party favor, watch, THE GREATEST, BITTERSUITE, la'mour de ma vie, overheated, oxytocin, male fantasy, skinny, 
idontwannabeyouanymore, blue and your power I KNOW IT'S A LOT but I really do love all these songs, even now while writing this. <br>
Her songs motivate me and they even help me when I feel like nothing can, I feel a deep connection with some of her songs. And I'm
really thankful to her in way. Even though she'll probably never know this I'm still very grateful for her.
(it's almost 3 am for me so please don't mind my writing mistakes (｡･･｡) )
    </div>
    <div class="top">
        Song Title	      Streams	Daily <br>
<button on:click={playsound1}> lovely(with Khalid)</button>,  <br>
3,517,817,499	1,364,954 <br>
<button on:click={playsound2}> BIRDS OF A FEATHER </button>, <br>
3,166,549,281	3,369,065 <br>
<button on:click={playsound3}>bad guy</button>,  <br>
2,818,342,043	761,711 <br>
<button on:click={playsound4} > when the party's over</button>, <br>
2,335,923,909	1,026,827 <br>
<button on:click={playsound5}>everything I wanted</button> <br>
1,983,218,755	766,714 <br>
<button on:click={playsound6}>ocean eyes</button> <br>
1,967,593,992	1,479,198 <br>
<button on:click={playsound7}>Happier Than Ever</button> <br>
1,703,999,326	829,156 <br>
<button on:click={playsound8}>WILDFLOWER</button> <br>
1,627,622,919	2,450,414 <br>
<button on:click={playsound9}>What Was I Made For?</button> [From The Movie "Barbie"] <br>
1,460,749,518	938,887 <br>
<button on:click={playsound10}>idontwannabeyouanymore</button> <br>
1,299,421,779	400,815 <br>
    </div>
    <div class="tour">
THE REST OF HER TOUR DATES: <br>
Nov 7 & 8, 2025 — Smoothie King Center, New Orleans, LA <br>

 • Nov 10 & 11, 2025 — BOK Center, Tulsa, OK <br>


 • Nov 13 & 14, 2025 — Moody Center ATX, Austin, TX <br>


 • Nov 18 & 19, 2025 — PHX Arena (Mortgage Matchup Center), Phoenix, AZ <br>


 • Nov 22 & 23, 2025 — Chase Center, San Francisco, CA <br>
    </div>
    <div class="poll">
<h2>Which is ur fav Billie album?</h2>
{#each albums as album}
<button on:click={() => vote(album)}>{album.name}</button>
{/each}
<h3>Results:</h3>
{#each albums as album}
    <p>{album.name}: {album.votes}</p>
  {/each}
    </div>
    <div class="comments">
        <h2>Leave acomment for Billie!</h2>
        <input type="text" bind:value={comment} placeholder="Write something..."/>
        <button on:click={addcomment}>Post</button>
        <ul>
            {#each comments as c}
      <li>{c}</li>
    {/each}
  </ul>
    </div>
    <img src="https://i.pinimg.com/736x/5e/b6/0c/5eb60c9bf11d2185f671ced40bc9d2c2.jpg" 
    alt="billie album"
    class="album"
    >
    <img src="https://scontent.fotp3-1.fna.fbcdn.net/v/t1.15752-9/568658292_2245292135973686_237013872248418856_n.jpg?stp=dst-jpg_s552x414_tt6&_nc_cat=107&ccb=1-7&_nc_sid=0024fc&_nc_ohc=6ssD9PcCFeIQ7kNvwG0m3vt&_nc_oc=AdkxffvVNCKIB84sazpc44pv_m2CdiTs2KLXR0wxqSud26SRlLwpqiDQTjF9ugJadxs&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent.fotp3-1.fna&oh=03_Q7cD3wEZQu0f0q6eAYQofWeOjHA4gCDF488cIQxW3glcybOpDA&oe=692D155E" 
    alt="billie flag"
    class="flag"
    >
</main>
<style>
    main {
         padding:0;
        margin: 0;
        background-image: url(https://i.pinimg.com/736x/ff/64/38/ff64386342389214d8a0652fbcb3fa19.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        min-height: 125vh;
        padding-top: 20px;
       
    }
    h1.site-title {
        color: royalblue;
        text-align: center;
        font-weight:900px ;
        font-size: 50px;
        font-family: 'Cutout', sans-serif;
        margin: 0;
        padding: 0;
    }
    
    .billie {
        background-image: url(https://scontent.fotp3-4.fna.fbcdn.net/v/t1.15752-9/569206871_841929824900655_2062461056248950267_n.jpg?stp=dst-jpg_p480x480_tt6&_nc_cat=110&ccb=1-7&_nc_sid=0024fc&_nc_ohc=ChHRY7OGD7YQ7kNvwGt01hs&_nc_oc=AdnUm5xJqEuuvavsE6LtGD2x5qzftJPHCjVYgBqZcBk2jVx3ozxVO_4MJ_Lp872OBKU&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent.fotp3-4.fna&oh=03_Q7cD3wGE9Jh92vmR5vXZe70Xiw_1GgPPfYJcfVS1qRYHTGJNnw&oe=692CC01A);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: top center;
        height: 800px;
        width: 90%;
        max-width: 425px;
        border-radius: 10px;
        margin: 40px;
        padding-top: 40px;
        padding-left: 30px;
        padding-right: 20px;
        padding-bottom: 0px;
        color: beige;
        backdrop-filter: blur(4px);
        font-size: 18px;
    }
    .top {
        background-image: url(https://scontent.fotp3-2.fna.fbcdn.net/v/t1.15752-9/569326635_817064641187548_4800407470699700563_n.jpg?stp=dst-jpg_p480x480_tt6&_nc_cat=105&ccb=1-7&_nc_sid=0024fc&_nc_ohc=GNNAyEhOM3YQ7kNvwHejEgC&_nc_oc=Adkfvy-I1Ri9upH8ISt20rBI6m2iBa5KQsKmluN31dWuwMukKjfUqfWVZB9HrDYmM5I&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent.fotp3-2.fna&oh=03_Q7cD3wGGtwa_l_rSj0OdVD1qkYu0Rq9Spsa-7KNTX4m4Qyjhhg&oe=692CC974);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: top center;
        height: 500px;
        width: 90%;
        max-width: 300px;
        margin-left: 1400px;
        margin-top: -750px;
        position: absolute;
        padding-top: 75px;
        padding-left: 60px;
        padding-right: 60px;
        padding-bottom: 90px;
        font-size: 18px;
        color: darkblue;
    }
    .tour {
        background-image: url(https://scontent.fotp3-4.fna.fbcdn.net/v/t1.15752-9/569883976_1835731307039627_3975600273268688239_n.jpg?stp=dst-jpg_p480x480_tt6&_nc_cat=100&ccb=1-7&_nc_sid=0024fc&_nc_ohc=UbOQLTiH7cUQ7kNvwF17Y46&_nc_oc=Admi0hEqGyehI5xj4iK8XpSpOVftZ3DyO6VRxxlfBB9ShMzYajSFAjSF0vjBjnc_Zu8&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent.fotp3-4.fna&oh=03_Q7cD3wGN73lZG_BTXKsvKXnkyMX3CXeQBmwyh-bliJCDbmwFMA&oe=692CF49C);
        background-position: top center;
        background-repeat: no-repeat;
        background-size: cover;
        height: 350px;
        width: 90%;
        max-width: 200px;
        margin-top: -500px;
        position: absolute;
        margin-left: 1050px;
        padding: 60px;
        padding-top: 90px;
    }
    .poll {
    background-color: royalblue;
    color: lightyellow;
    padding: 20px;
    border-radius: 10px;
    width: 300px; 
    font-family: 'Arial', sans-serif;
    top: 200px;
    left: 600px;
    position: absolute;
    }
    .comments {
        background-color: darkblue;
        color: lightblue;
        padding: 20px;
        border-radius: 10px;
        width: 350px;
        margin: 20px;
         font-family: Arial, sans-serif;
         left: 600px;
         position: absolute;
         top: 600px;
    }
    .album {
     height: 350px;
    width: 90%;
    max-width: 400px;
    margin-left: 950px;
    margin-top: -875px;
    position: absolute;
    }
    .flag {
        height: 350px;
        width: 90%;
        max-width: 500px;
        margin-left: 535px;
        top: 775px;
        position: absolute;
    }
</style>