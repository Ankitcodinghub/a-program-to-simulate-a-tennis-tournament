# a-program-to-simulate-a-tennis-tournament
**TO GET THIS SOLUTION VISIT:** [A program to simulate a tennis tournament](https://www.ankitcodinghub.com/product/a-program-to-simulate-a-tennis-tournament/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;9083&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;A program  to simulate a tennis tournament&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
The program is to simulate a tennis tournament which takes a field of 8 players and plays a series of three rounds, eliminating half the players with each round – ending with a single (winning) player.

Individual rounds operate as follows:

? Randomly divide the remaining players into pairs. ?

Simulate a single game between each pair, using the scoring rules specified in below. ?

The winners advance to the next round, the losers are eliminated.

The user should enter the names of the 8 players, then the program should simulate each of the three rounds, printing the result of each game.

At the end of the tournament the program should print the name of the winner and the name of the second place finisher.

Your software must include appropriate classes of object for both a player and a tournament, but beyond that the design is at your discretion.

In addition, the simulation between any two players is as follows:

? The score will start at 0/0, and will continue until someone wins the game. ?

It is assumed that either player one or player two will win a point on each play. ?

A (pseudo) random number generator will be used to determine the results of each play, with each player equally likely to win any given point. ?

After each play, the program should indicate which player won the point, the new score, and which player is serving next. The program should then pause until the user strikes a key to continue play. ?

The player who won the previous point serves for the next point (randomly determine the player to serve first in the game). ?

The score is determined as follows (scores displayed as server/receiver).

Previous Score 0/0 0/15 0/30 0/40 15/0 15/15 15/30 15/40 30/0 30/15 30/30 30/40 40/0 40/15 40/30 deuce advantage

Server wins point 15/0 15/15 15/30 15/40 30/0 30/15 30/30 30/40 40/0 40/15 40/30 deuce game game game advantage game

Receiver wins point 0/15 0/30 0/40 game 15/15 15/30 15/40 game 30/15 30/30 30/40 game 40/15 40/30 deuce advantage deuce

Here is my code so far:

import java.util.*;

import java.util.Random;

import java.util.Collections;

import java.util.ArrayList;

public class assignmentz

{

public static void main (String args[])

{

System.out.println(“Quick Note:”);

System.out.println(“SR = Server RR = Receiver AD = Advantage DD = Deuce”);

Player player = new Player();

Tournament tournament = new Tournament();

tournament.game();

}

}

class Player

{

private ArrayList&lt;String&gt; name;

private ArrayList&lt;String&gt; players;

public Player ()

{

name = new ArrayList&lt;String&gt;();

players = new ArrayList&lt;String&gt;();

}

public ArrayList&lt;String&gt; namePlayers ()

{

Scanner input = new Scanner(System.in);

System.out.println(“Enter a name for each player.”);

for (int i = 0; i &lt; 8; i++)

{

System.out.print(“Player” + (i + 1) + “: “);

name.add(input.nextLine());

}

return name;

}

public ArrayList&lt;String&gt; randomizePlayers (ArrayList&lt;String&gt; name)

{

ArrayList&lt;String&gt; team = new ArrayList&lt;String&gt;();

ArrayList&lt;String&gt; newList = new ArrayList&lt;String&gt;();

team = namePlayers();

Collections.shuffle(team);

return team;

}

}

class Tournament

{

Player player = new Player();

private ArrayList&lt;String&gt; name;

public Tournament ()

{

name = new ArrayList&lt;String&gt;();

}

public void roundOne (ArrayList&lt;String&gt; name)

{

name = player.randomizePlayers(name); //four matches

System.out.println(“nt Round One”);

int k = 0;

System.out.println(“Match 1 Match 2 Match 3 Match 4”);

System.out.println(“SR RR SR RR SR RR SR RR”);

System.out.println(“0 0 0 0 0 0 0 0″);

for(int i = 0; i &lt; 4; i++)

{

for(int t = 0; t &lt; 1; t++)

{

System.out.print(” ” + name.get(k) + ” “);

k++;

System.out.print(name.get(k) + ” “);

k++;

}

}

System.out.println();

pointsGenerator();

}

public void roundTwo (ArrayList&lt;String&gt; name)

{

//two matches

System.out.println(“Round Two”);

player.randomizePlayers(name);

}

public void roundThree (ArrayList&lt;String&gt; name)

{

System.out.println(“Final Round”);

player.randomizePlayers(name);

}

public int pointsGenerator ()

{

return 1;

}

public void game()

{

roundOne(name);

//roundTwo(name);

//roundThree(name);

}

}
