var Top_of_the_Hot_list_and_Cool_Hopper_Acheived = true;
//Change this to false if you don't want cool Hopper over your other character...

var computerScore = false;

/* Voting Record (Time after made):
 - Less than 1 minute: 2 votes
 - about 5 minutes: 3 votes
 - Day 1: 118 votes (2nd on the Hot List!... my record!)
 - Day 2: 251 votes (1st on the Hot List!... broke my last record!)
 - Day 3: 335 votes (Still first on the Hot List!)
 - Day 4: 350 votes (Back to 4th on the Hot List)
*/
var votes = [
    ["1 min",2,"Wow! That's fast!"],
    ["±5 min",3,"3 votes in less than 10 min?"],
    ["Day 1",118,"Over 100 votes!"],
    ["Day 2",251,"Another 100 votes in 1 day!"],
    ["Day 3",335,"Another day on the top of the Hot List!"],
    ["Day 4",350,"The streaks going done now..."],
];
var Cx = 0;
var type = "line";

var page = "logo";
var who = ""; //If you already have a score on the score board put the exact name used in the score board so that it will show you where you would be in the score board!

//Scores
var partition=function(array, p, r){
    //swap function
    var swap = function(array, p, r){
        var temp = array[p];
        array[p] = array[r];
        array[r] = temp;
    };
    
    var i = p;
    for (var j = p; j < r; j++) {
        if (array[j][0] <= array[r][0]) {
            swap(array, j, i);
            i++;
        }
    }
    swap(array, r, i);
    return i;
};
var quickSort = function(array, p, r) {
    if(p < r){
        var q = partition(array, p, r);
        quickSort(array, p, q-1);
        quickSort(array, q+1, r);
    }
};
var sy = 0;
var scores = [
    /* [score, name] */
    [2558,"👀 Jᾀ¢ϕɓ ℋϕɼŋɓἕ¢ḳ 👀",getImage("creatures/Hopper-Cool")],
    [677,"Izek",getImage("avatars/mr-pink-orange")],
    [165,"Bazookaboy23",getImage("avatars/primosaur-ultimate")],
    [718,"Johanna Russo",getImage("avatars/aqualine-ultimate")],
    [732,"⊷נαck ρ.⊶",getImage("avatars/orange-juice-squid")],
    [716,"GameChief999",getImage("avatars/leaf-grey")],
    [272,"leytonwinkler",getImage("avatars/leaf-blue")],
    [800,"ScusX",getImage("creatures/Hopper-Cool")],
    [121,"Lara",getImage("creatures/Hopper-Jumping")],
    [9234,"Stephen",getImage("avatars/aqualine-ultimate")],
    [364,"KingChainZ",getImage("creatures/BabyWinston")],
    [178,"SarveshGade",getImage("avatars/starky-ultimate")],
    [529,"TooMuchSchool",getImage("avatars/starky-ultimate")],
    [561,"isamhanif",getImage("avatars/starky-sapling")],
    [792,"ButterBurr",getImage("creatures/OhNoes")],
    [319,"Nicholas Wang",getImage("avatars/leaf-blue")],
    [637,"👾Vader2003™👾",getImage("avatars/starky-seed")],
    [860,"BlackjediCa",getImage("avatars/starky-tree")],
    [726,"The #1 ShadΦw Proponent",getImage("avatars/starky-tree")],
    [884,"EP1X WARR10R",getImage("avatars/piceratops-ultimate")],
    [910,"DevinDumont",getImage("avatars/duskpin-ultimate")],
    [431,"Revolutionkiteman",getImage("avatars/starky-ultimate")],
    [407,"Kim Min",getImage("avatars/marcimus-purple")],
    [1219,"DerrekT. AlecIsBae",getImage("avatars/robot_female_2")],
    [753,"Leo Valdez",getImage("avatars/starky-sapling")],
    [3187,"Emma Brun",getImage("avatars/duskpin-ultimate")],
    [311,"Johnny Corcoran",getImage("avatars/robot_male_1")],
    [409,"jiraiya-the toad sage",getImage("creatures/Hopper-Happy")],
    [405,"CarterDougherty",getImage("avatars/aqualine-ultimate")],
    [640,"Literally Void",getImage("avatars/mr-pants-orange")],
    [695,"roatre11",getImage("avatars/duskpin-ultimate")],
    [562,"⊚♦AsнεηSκy♦⊚",getImage("avatars/piceratops-sapling")],
    [721,"Rand☢mWeirdo204",getImage("avatars/aqualine-ultimate")],
    [310,"Grandma'sCheese",getImage("creatures/OhNoes")],
    [740,"💖✨ANGELA AHN✨💖",getImage("creatures/Hopper-Jumping")],
    [613,"PhineasGreene",getImage("avatars/primosaur-ultimate")],
    [247,"ICanBuildAnything",getImage("avatars/robot_male_2")],
    [2198,"Jakeb01",getImage("avatars/robot_male_1")],
    [604,"Ben",getImage("avatars/leaf-green")],
    [800,"Vortex Programming",getImage("avatars/robot_female_1")],
    [282,"Alexa Sano",getImage("avatars/duskpin-sapling")],
    [434,"JosiahJoel2",getImage("avatars/mr-pants-purple")],
    [1649,"SpectrumNight",getImage("avatars/duskpin-ultimate")],
    [438,"#Buchholz1",getImage("avatars/primosaur-ultimate")],
    [10014,"CPU",getImage("avatars/avatar-team")],
    [742,"Drye10",getImage("avatars/starky-ultimate")],
    [721,"Gamer_God",getImage("avatars/aqualine-ultimate")],
    [886,"Yossi Soffer",getImage("avatars/primosaur-sapling")],
    [1024,"Thomas Jureidini",getImage("creatures/Hopper-Happy")],
    [1036,"Ruthford",getImage("creatures/Winston")],
    [364,"Rangerfox7047",getImage("avatars/purple-pi-teal")],
    [578,"The Geckoverlord",getImage("avatars/old-spice-man")],
    [108,"Kaden H.",getImage("avatars/leaf-green")],
    [414,"Kanghoon",getImage("avatars/starky-sapling")],
    [303,"CocoaBean1",getImage("avatars/piceratops-ultimate")],
    [12430,"мαgιcѕqυιяяєℓ",getImage("avatars/orange-juice-squid")],
    //[,"",getImage("cute/none")],
];
quickSort(scores,0,scores.length-1);

//Game
{
size(400,400,P2D/* I didn't know what the 3rd parameter was supposed to be so I guessed */);
//Credit to Izek for the following two functions

var sum = function(arr) {
    var num = 0;
    for (var i = 0; i<arr.length; i++) {
        num+=arr[i];
    }
    return num;
};

var keys = [];
keyPressed = function() {
    keys[keyCode]=true;
};
keyReleased = function() {
    keys[keyCode]=false;
};

var bullet = function(x,y,xv,yv) {
    this.pos = new PVector(x,y);
    this.vel = new PVector(xv,yv);
    this.count = 0;
    this.draw = function() {
        rectMode(CENTER);
        var angle = this.vel.heading();
        pushMatrix();
        translate(this.pos.x,this.pos.y);
        scale(0.3);
        rotate(angle);
        noStroke();
        fill(this.color);
        rect(0,0,30,10);
        triangle(15,-5,15,5,30,0);
        quad(-15,-4,-5,-4,-15,-12,-20,-12);
        quad(-15,4,-5,4,-15,12,-20,12);
        popMatrix();
    };
    this.update = function() {
        this.pos.add(this.vel);
        this.vel.limit(4);
        if (this.pos.x>width-width/3) {
            this.vel.x = -2.5;
            this.vel.y = -3.5;
        }
        if (this.pos.x<width/3) {
            this.vel.x = 2.5;
            this.vel.y = -3.5;
        }
    };
    this.applyForce = function(f) {
        f.normalize();
        this.vel.add(new PVector(f.x,f.y/10));
    };
};
var bts = [];

var Gem = function(x,y,t,s) {
    this.p = new PVector(x,y);
    this.v = new PVector(0,0);
    this.t = t;
    this.s = s;
    this.c = 0;
    this.ti = 30;
    this.collecting = false;
    this.draw = function() {
        pushMatrix();
        translate(this.p.x,this.p.y);
        switch (this.t.toLowerCase()) {
            case "ruby":
                this.c = 10;
                {
                noStroke();
                fill(255, 51, 51);
                beginShape();
                vertex(-this.s/2,-this.s*1.2);
                vertex(this.s/2,-this.s*1.2);
                vertex(this.s/1.2,-this.s/1.25);
                vertex(this.s/1.2,this.s/1.25);
                vertex(this.s/2,this.s*1.2);
                vertex(-this.s/2,this.s*1.2);
                vertex(-this.s/1.2,this.s/1.25);
                vertex(-this.s/1.2,-this.s/1.25);
                vertex(-this.s/2,-this.s*1.2);
                endShape();
                //Shadows
                {
                fill(0,0,0,40);
                beginShape();
                vertex(this.s/2,-this.s*1.2);
                vertex(this.s/1.2,-this.s/1.25);
                vertex(this.s/1.2,this.s/1.25);
                vertex(this.s/2,this.s*1.2);
                vertex(-this.s/2,this.s*1.2);
                endShape();
                beginShape();
                vertex(this.s/1.2,-this.s/1.25);
                vertex(this.s/1.2,this.s/1.25);
                vertex(this.s/2,this.s*1.2);
                vertex((this.s/2)/1.7,(this.s*1.2)/1.7);
                vertex(this.s/1.2/1.7,this.s/1.25/1.7);
                vertex(this.s/1.2/1.7,-this.s/1.25/1.7);
                endShape();
                beginShape();
                vertex(this.s/1.2,this.s/1.25);
                vertex(this.s/2,this.s*1.2);
                vertex((this.s/2)/1.7,(this.s*1.2)/1.7);
                vertex((this.s/1.2)/1.7,(this.s/1.25)/1.7);
                endShape();
                fill(0,0,0,20);
                beginShape();
                vertex(this.s/2,-this.s*1.2);
                vertex(this.s/1.2,-this.s/1.25);
                vertex(this.s/1.2,this.s/1.25);
                vertex(this.s/2,this.s*1.2);
                vertex(-this.s/2,this.s*1.2);
                endShape();
                beginShape();
                vertex(-this.s/1.2,-this.s/1.25);
                vertex(-this.s/1.2,this.s/1.25);
                vertex(-this.s/2,this.s*1.2);
                vertex(-(this.s/2)/1.7,(this.s*1.2)/1.7);
                vertex(-this.s/1.2/1.7,this.s/1.25/1.7);
                vertex(-this.s/1.2/1.7,-this.s/1.25/1.7);
                endShape();
                beginShape();
                vertex(-this.s/1.2,this.s/1.25);
                vertex(-this.s/2,this.s*1.2);
                vertex(-(this.s/2)/1.7,(this.s*1.2)/1.7);
                vertex(-(this.s/1.2)/1.7,(this.s/1.25)/1.7);
                endShape();
                }
                pushMatrix();
                scale(0.65,0.7);
                fill(235, 47, 47);
                beginShape();
                vertex(-this.s/2,-this.s*1.2);
                vertex(this.s/2,-this.s*1.2);
                vertex(this.s/1.2,-this.s/1.25);
                vertex(this.s/1.2,this.s/1.25);
                vertex(this.s/2,this.s*1.2);
                vertex(-this.s/2,this.s*1.2);
                vertex(-this.s/1.2,this.s/1.25);
                vertex(-this.s/1.2,-this.s/1.25);
                vertex(-this.s/2,-this.s*1.2);
                endShape();
                popMatrix();
                }
            break;
            case "diamond":
                this.c = 50;
                {
                noStroke();
                fill(68,191,251);
                beginShape();
                vertex(this.s/3,-this.s/3);
                vertex(this.s/3,this.s/4);
                vertex(this.s,0);
                vertex(this.s/1.5,-this.s/1.7);
                endShape();
                beginShape();
                vertex(-this.s/3,-this.s/3);
                vertex(-this.s/3,this.s/4);
                vertex(-this.s,0);
                vertex(-this.s/1.5,-this.s/1.7);
                endShape();
                fill(190,239,254);
                beginShape();
                vertex(-this.s/3,-this.s/3);
                vertex(-this.s/1.5,-this.s/1.7);
                vertex(-this.s/3,-this.s/1.2);
                vertex(this.s/3,-this.s/1.2);
                vertex(this.s/1.5,-this.s/1.7);
                vertex(this.s/3,-this.s/3);
                endShape();
                fill(125,225,253);
                beginShape();
                vertex(this.s/3,-this.s/3);
                vertex(this.s/3,this.s/4);
                vertex(-this.s/3,this.s/4);
                vertex(-this.s/3,-this.s/3);
                endShape();
                fill(45, 148, 196);
                beginShape();
                vertex(0,this.s/1.2);
                vertex(-this.s/3,this.s/4);
                vertex(this.s/3,this.s/4);
                vertex(0,this.s/1.2);
                endShape();
                fill(17, 114, 184);
                beginShape();
                vertex(0,this.s/1.2);
                vertex(-this.s,0);
                vertex(-this.s/3,this.s/4);
                vertex(0,this.s/1.2);
                endShape();
                beginShape();
                vertex(0,this.s/1.2);
                vertex(this.s,0);
                vertex(this.s/3,this.s/4);
                vertex(0,this.s/1.2);
                endShape();
                }
            break;
            case "emerald":
                this.c = 5;
                {
                noStroke();
                fill(115,197,37);
                beginShape();
                vertex(-this.s,0);
                vertex(-this.s/sqrt(2),this.s/sqrt(2));
                vertex(0,this.s);
                vertex(this.s/sqrt(2),this.s/sqrt(2));
                vertex(this.s,0);
                vertex(this.s/sqrt(2),-this.s/sqrt(2));
                vertex(0,-this.s);
                vertex(-this.s/sqrt(2),-this.s/sqrt(2));
                endShape();
                fill(0,0,0,60);
                beginShape();
                vertex(0,0);
                vertex(-this.s/sqrt(2),this.s/sqrt(2));
                vertex(0,this.s);
                endShape();
                beginShape();
                vertex(0,0);
                vertex(-this.s,0);
                vertex(-this.s/sqrt(2),this.s/sqrt(2));
                vertex(0,this.s);
                vertex(this.s/sqrt(2),this.s/sqrt(2));
                endShape();
                beginShape();
                vertex(0,0);
                vertex(-this.s/sqrt(2),-this.s/sqrt(2));
                vertex(-this.s,0);
                vertex(-this.s/sqrt(2),this.s/sqrt(2));
                vertex(0,this.s);
                vertex(this.s/sqrt(2),this.s/sqrt(2));
                vertex(this.s,0);
                endShape();
                fill(255,255,255,70);
                beginShape();
                vertex(0,0);
                vertex(this.s/sqrt(2),-this.s/sqrt(2));
                vertex(0,-this.s);
                endShape();
                fill(115,197,37);
                pushMatrix();
                scale(0.55);
                beginShape();
                vertex(-this.s,0);
                vertex(-this.s/sqrt(2),this.s/sqrt(2));
                vertex(0,this.s);
                vertex(this.s/sqrt(2),this.s/sqrt(2));
                vertex(this.s,0);
                vertex(this.s/sqrt(2),-this.s/sqrt(2));
                vertex(0,-this.s);
                vertex(-this.s/sqrt(2),-this.s/sqrt(2));
                endShape();
                popMatrix();
                }
            break;
            case "tri-emerald":
                this.c = 25;
                {
                noStroke();
                fill(255,174,66);
                beginShape();
                vertex(0,-this.s*1.2);
                vertex(this.s*cos(30)*1.2,this.s*sin(30)*1.2);
                vertex(-this.s*cos(30)*1.2,this.s*sin(30)*1.2);
                endShape();
                fill(255,214,157);
                beginShape();
                vertex(0,-this.s/1.8);
                vertex(this.s*cos(30)/1.8,this.s*sin(30)/1.8);
                vertex(-this.s*cos(30)/1.8,this.s*sin(30)/1.8);
                endShape();
                fill(249,148,47);
                beginShape();
                vertex(this.s*cos(30)/1.8,this.s*sin(30)/1.8);
                vertex(-this.s*cos(30)/1.8,this.s*sin(30)/1.8);
                vertex(-this.s*cos(30)*1.2,this.s*sin(30)*1.2);
                vertex(this.s*cos(30)*1.2,this.s*sin(30)*1.2);
                endShape();
                fill(255,191,107);
                beginShape();
                vertex(0,-this.s/1.8);
                vertex(0,-this.s*1.2);
                vertex(this.s*cos(30)*1.2,this.s*sin(30)*1.2);
                vertex(this.s*cos(30)/1.8,this.s*sin(30)/1.8);
                endShape();
                }
            break;
            case "black-diamond":
                this.c = 100;
                {
                noStroke();
                fill(72,72,72);
                beginShape();
                vertex(-this.s/1.5,0);
                vertex(-this.s/1.5/1.5,-(this.s*1.5+0)/3);
                vertex(0,0);
                endShape();
                fill(46,46,46);
                beginShape();
                vertex(-this.s/1.5,0);
                vertex(-this.s/1.5/1.5,(this.s*1.5+0)/3);
                vertex(0,0);
                endShape();
                fill(72,72,72);
                beginShape();
                vertex(this.s/1.5,0);
                vertex(this.s/1.5/1.5,(this.s*1.5+0)/3);
                vertex(0,0);
                endShape();
                fill(127,127,127);
                beginShape();
                vertex(this.s/1.5,0);
                vertex(this.s/1.5/1.5,-(this.s*1.5+0)/3);
                vertex(0,0);
                endShape();
                fill(206,206,206);
                beginShape();
                vertex(0,-this.s*1.5);
                vertex(this.s/1.5/1.5,-(this.s*1.5+0)/3);
                vertex(0,0);
                endShape();
                fill(127,127,127);
                beginShape();
                vertex(0,0);
                vertex(-this.s/1.5/1.5,-(this.s*1.5+0)/3);
                vertex(0,-this.s*1.5);
                endShape();
                fill(46,46,46);
                beginShape();
                vertex(0,this.s*1.5);
                vertex(this.s/1.5/1.5,(this.s*1.5+0)/3);
                vertex(0,0);
                endShape();
                fill(18,18,18);
                beginShape();
                vertex(0,0);
                vertex(-this.s/1.5/1.5,(this.s*1.5+0)/3);
                vertex(0,this.s*1.5);
                endShape();
                fill(172,172,172);
                beginShape();
                vertex(0,-this.s*1.5/3);
                vertex(this.s/1.5/3,0);
                vertex(0,this.s*1.5/3);
                vertex(-this.s/1.5/3,0);
                endShape();
                }
            break;
        }
        popMatrix();
    };
    this.update = function() {
        this.p.add(this.v);
        this.v.limit(5);
    };
};
var gems = [];
var types = ["emerald","ruby","tri-emerald","diamond","black-diamond"];

var Player = function(x,y,comp,t,u) {
    this.y = y;
    this.pos = new PVector(x,this.y);
    this.vel = new PVector(0,-2);
    this.returnVel = -2;
    this.spd = 3;
    
    this.gs = 0;
    this.dead = false;
    
    this.score = 0;
    this.high = 0;
    this.prev = 0;
    
    this.computer = comp;
    this.u = u;
    this.t = t;
    this.total = 0;
    
    switch (this.t.toLowerCase()) {
        case "default":
            this.cost = "N/A";
        break;
        case "check":
            this.cost = 15*3;
        break;
        case "water":
            this.cost = 25*3;
        break;
        case "lava":
            this.cost = 40*3;
        break;
        case "glitch":
            this.cost = 70*3;
        break;
        case "earth":
            this.cost = 150*2;
        break;
    }
    
    this.sheild = false;
    this.sheildT = 40;
    this.gemMagnet = false;
    this.gemT = 30;
    this.bullet = false;
    
    this.on = false;
    this.right = true;
    this.left = false;
    this.r = 0;
    
    this.gms = [];
    for (var i = 0; i<types.length; i++) {
        this.gms.push(new Gem(0,0,types[i],5));
    }
    
    this.v = [];
    this.v1 = [];
    this.v2 = [];
    this.b = [];
    
    for (var i = 0; i<6; i++) {
        this.v.push(new PVector(20*cos(0)+this.pos.x,20*sin(0)+this.pos.y));
        this.v1.push(new PVector(20*cos(0)+this.pos.x,20*sin(0)+this.pos.y));
    }
    
    this.ps = [];
    this.ss = [];
    this.vs = [];
    for (var i = 0; i<5; i++) {
        for (var j = 0; j<5; j++) {
            this.ps.push(new PVector(i*2-4,j*2-4));
            this.vs.push(new PVector(random(-3,3),random(-8,-5)));
            this.ss.push(new PVector(i*2-4,j*2-4));
        }
    }
    
    this.draw = function() {
        pushMatrix();
        translate(this.pos.x,this.pos.y);
        rotate(this.r);
        noStroke();
        rectMode(CENTER);
        for (var i in this.ps) {
            switch (this.t.toLowerCase()) {
                case "default":
                    noStroke();
                    fill(0);
                break;
                case "glitch":
                    if (frameCount%i===0) {
                        fill(0,0,0);
                    }
                    else {
                        noFill();
                    }
                break;
                case "check":
                    noStroke();
                    if (i%2===0) {
                        fill(0);
                    }
                    else {
                        fill(255,255,255);
                    }
                break;
                case "earth":
                    noStroke();
                    fill(0,noise(i/5,56)*255,0);
                break;
                case "water":
                    fill(0,0,noise(i/5,frameCount/20)*255);
                break;
                case "lava":
                    fill(255, noise(i/5,frameCount/20)*255, 0);
                break;
            }
            rect(this.ps[i].x,this.ps[i].y,2,2);
        }
        if (this.t.toLowerCase()==="glitch" && !this.dead) {
            noFill();
            stroke(0);
            strokeWeight(1);
            rect(0,0,10,10);
        }
        popMatrix();
        if (!this.dead && this.t.toLowerCase()==="earth") {
            stroke(0,100,0);
            noFill();
            strokeWeight(1);
            beginShape();
            for (var v in this.v) {
                curveVertex(this.v[v].x,this.v[v].y);
                this.v[v].x = 20*cos(frameCount*2+v*30)+this.pos.x;
                this.v[v].y = 30*sin(frameCount*3+v*30)+this.pos.y;
            }
            endShape();
            beginShape();
            for (var v in this.v1) {
                curveVertex(this.v1[v].x,this.v1[v].y);
                this.v1[v].x = -30*cos(frameCount*3+v*30)+this.pos.x;
                this.v1[v].y = -20*sin(frameCount+v*30)+this.pos.y;
            }
            endShape();
        }
        if (!this.dead && this.sheild) {
            stroke(0,0,0);
            noFill();
            strokeWeight(1);
            beginShape();
            for (var v in this.v) {
                curveVertex(this.v[v].x,this.v[v].y);
                this.v[v].x = 20*cos(frameCount*2+v*30)+this.pos.x;
                this.v[v].y = 30*sin(frameCount*3+v*30)+this.pos.y;
            }
            endShape();
            beginShape();
            for (var v in this.v1) {
                curveVertex(this.v1[v].x,this.v1[v].y);
                this.v1[v].x = -30*cos(frameCount*3+v*30)+this.pos.x;
                this.v1[v].y = -20*sin(frameCount+v*30)+this.pos.y;
            }
            endShape();
        }
        if (Top_of_the_Hot_list_and_Cool_Hopper_Acheived===true && !this.dead) {
            pushMatrix();
            translate(this.pos.x,this.pos.y);
            rotate(this.r);
            imageMode(CENTER);
            image(getImage("creatures/Hopper-Cool"),0,0,20,20);
            popMatrix();
        }
        for (var i in this.gms) {
            this.gms[i].p.x = this.pos.x+30*cos(frameCount*3+i*40+i*cos(frameCount*5+i*10)*10);
            this.gms[i].p.y = this.pos.y+30*sin(frameCount*3+i*40+i*cos(frameCount*5+i*10)*10);
            this.gms[i].s = this.gs;
            this.gms[i].draw();
        }
        if (this.gemMagnet===true) {
            if (this.gs<=5) {
                this.gs+=0.2;
            }
        }
        if (this.gemMagnet===false) {
            if (this.gs>0) {
                this.gs-=0.2;
            }
        }
    };
    this.update = function(o,b) {
        switch (this.t.toLowerCase()) {
            case "default":
                this.spd = 3;
            break;
            case "check":
                this.spd = 3.5;
            break;
            case "water":
                this.spd = 3.75;
            break;
            case "lava":
                this.spd = 4;
            break;
            case "glitch":
                this.spd = 2.75;
            break;
            case "earth":
                this.spd = 3;
            break;
        }
        this.pos.add(this.vel);
        this.vel.limit(50);
        this.vel.x = constrain(this.vel.x, -this.spd, this.spd);
        if (this.pos.x-4<width/3) {
            this.on = true;
            this.pos.x = width/3+4;
            this.vel.x = 0;
        }
        else if (this.pos.x+4>width-width/3) {
            this.on = true;
            this.pos.x = width-width/3-4;
            this.vel.x = 0;
        }
        else if (this.wall(b)) {
            for (var i in b) {
                if (this.pos.x+5>b[i].pos.x-7 && this.pos.x-5<b[i].pos.x+7 &&
                this.pos.y+5>b[i].pos.y-2 && this.pos.y-5<b[i].pos.y+2) {
                    if (b[i].t===1) {
                        if (this.vel.x>0) {
                            this.on = true;
                            this.pos.x = b[i].pos.x-12.5;
                            this.vel.x = 0;
                        }
                        if (this.vel.x<0) {
                            this.on = true;
                            this.pos.x = b[i].pos.x+12.5;
                            this.vel.x = 0;
                        }
                    }
                    if (b[i].t===2) {
                        if (this.right) {
                            this.on = true;
                            this.pos.x = b[i].pos.x-12.5;
                            this.vel.x = 0;
                            this.right = false;
                            this.left = true;
                        }
                        else if (this.left) {
                            this.on = true;
                            this.pos.x = b[i].pos.x+12.5;
                            this.vel.x = 0;
                            this.right = true;
                            this.left = false;
                        }
                    }
                }
            }
        }
        else {
            this.on = false;
        }
        if (!this.computer) {
            if (this.on && this.right && keys[LEFT]) {
                this.left = true;
                this.right = false;
            }
            if (this.on && this.left && keys[RIGHT]) {
                this.left = false;
                this.right = true;
            }
            if (mouseIsPressed) {
                if (this.on && this.right) {
                    this.left = true;
                    this.right = false;
                }
                else if (this.on && this.left) {
                    this.left = false;
                    this.right = true;
                }
                else {
                    if (this.on) {
                        this.left = true;
                        this.right = true;
                    }
                }
            }
        }
        if (this.computer) {
            for (var i in o) {
                if ((dist(o[i].pos.x,o[i].pos.y,this.pos.x,this.pos.y)<o[i].s*11-1) &&
                (this.on && o[i].pos.y<this.pos.y)){
                    if (this.right) {
                        this.right = false;
                        this.left = true;
                    }
                    else if (this.left) {
                        this.left = false;
                        this.right = true;
                    }
                    else {
                        this.left = true;
                        this.right = true;
                    }
                }
            }
        }
        
        if (!this.on) {
            if (this.right) {
                this.r+=12;
            }
            if (this.left) {
                this.r-=12;
            }
        }
        if (this.on) {
            if (Top_of_the_Hot_list_and_Cool_Hopper_Acheived===false) {
                this.r = 0;
            }
            if (Top_of_the_Hot_list_and_Cool_Hopper_Acheived===true) {
                if (this.pos.x<width/2) {
                    this.r = 90;
                }
                if (this.pos.x>width/2) {
                    this.r = -90;
                }
            }
        }
        this.pos.y = this.y;
        if (this.dead) {
            this.sheild = false;
            this.gemMagnet = false;
            for (var i in bts) {
                bts.splice(i,bts.length);
            }
            for (var i in this.ps) {
                this.ps[i].add(this.vs[i]);
                if (this.pos.x+this.ps[i].x<width/3 || this.pos.x+this.ps[i].x>width-width/3) {
                    this.vs[i].x *= -1;
                }
            }
            this.r = 0;
            this.vel.x = 0;
            this.vel.y = 0;
        }
        if (!this.dead) {
            this.score+=0.1;
        }
        this.vel.y -= 0.0001;
        this.applyForce(new PVector(100,0));
        
        if (!this.sheild) {
            this.sheildT = 20;
        }
        else {
            if (this.sheild) {
                this.sheildT -= 0.01;
            }
        }
        if (this.sheildT<=0) {
            this.sheild = false;
        }
        
        if (!this.gemMagnet) {
            this.gemT = 20;
        }
        else {
            if (this.gemMagnet) {
                this.gemT -= 0.01;
            }
        }
        if (this.gemT<=0) {
            this.gemMagnet = false;
        }
        
        if (this.bullet) {
            bts.push(new bullet(this.pos.x,this.pos.y,3,-random(abs(this.vel.y))));
            bts.push(new bullet(this.pos.x,this.pos.y,-3,-random(abs(this.vel.y))));
            this.bullet = false;
        }
    };
    this.applyForce = function(f) {
        f.normalize();
        if (this.right) {
            this.vel.add(new PVector(f.x,f.y));
        }
        if (this.left) {
            this.vel.add(new PVector(-f.x,f.y));
        }
    };
    this.applyGravity = function(force) {
        if (this.dead) {
            for (var i in this.vs) {
                this.vs[i].add(force);
            }
        }

    };
    this.collide = function(o) {
        if (this.t.toLowerCase()==="earth" || this.sheild) {
            for (var j in this.v) {
                for (var i in o) {
                    if (dist(o[i].pos.x,o[i].pos.y,this.v[j].x,this.v[j].y)<o[i].s) {
                        o.splice(i,1);
                    }
                }
            }
            for (var j in this.v1) {
                for (var i in o) {
                    if (dist(o[i].pos.x,o[i].pos.y,this.v1[j].x,this.v1[j].y)<o[i].s) {
                        o.splice(i,1);
                    }
                }
            }
        }
        for (var i in o) {
            if (dist(o[i].pos.x,o[i].pos.y,this.pos.x,this.pos.y)<o[i].s*1.5) {
                if (this.t.toLowerCase()!=="glitch" || (this.t.toLowerCase()==="glitch" && abs(floor(this.score%10))!==0)) {
                    if (abs(this.score)>this.high) {
                        this.high = abs(floor(this.score));
                    }
                    this.prev = abs(floor(this.score));
                    this.dead = true;
                }
            }
        }
    };
    this.wall = function(o) {
        for (var i in o) {
            if (this.pos.x+5>o[i].pos.x-7.5 && this.pos.x-5<o[i].pos.x+7.5 &&
            this.pos.y+5>o[i].pos.y-7.5 && this.pos.y-5<o[i].pos.y+7.5) {
                return true;
            }
        }
    };
};

var player = new Player(width/2,height-100,false,"default",true);
var homePlayer = new Player(width/2,height-100,true,"",true);
var Spike = function(h) {
    this.h = h;
    this.n = random();
    this.t = 0;
    var x;
    if (this.n>=0.5) {
        x = width-width/3+1;
        this.t = 1;
        if (this.n>0.65 && this.n<0.75) {
            x = random(width/3+30,width-width/3-30);
            this.t = 0;
        }
    }
    else {
        x = width/3-1;
        this.t = 1;
    }
    this.pos = new PVector(x,random(-45,-30));
    this.vel = new PVector(0,0);
    this.s = random(5,9);
    if (this.n>0.65 && this.n<0.75) {
        this.r = random(360);
        this.vel.x = 3;
    }
    else {
        this.r = 0;
    }
    this.draw = function() {
        if (this.n>0.65 && this.n<0.75) {
            this.pos.add(this.vel);
            this.t = 0;
            this.r+=20;
        }
        pushMatrix();
        translate(this.pos.x,this.pos.y);
        rotate(this.r);
        fill(50, 50, 50);
        if (this.pos.x<width/2 && this.t===1) {
            noStroke();
            triangle(0,-this.s,0,this.s,this.s*1.5,0);
        }
        else if (this.pos.x>width/2 && this.t===1) {
            noStroke();
            triangle(0,-this.s,0,this.s,-this.s*1.5,0);
        }
        else if (this.n>0.65 && this.n<0.75 && this.t===0) {
            rectMode(CENTER);
            strokeWeight(1);
            stroke(255,255,255);
            rect(0,0,this.s/1.5,this.s/1.5,-4);
        }
        if (this.pos.x>width-width/3) {
            this.vel.x = -3;
        }
        if (this.pos.x<width/3) {
            this.vel.x = 3;
        }
        popMatrix();
    };
};

var shop = [];
var ptypes = ["default","check","water","lava","glitch","earth"];
var htype = 0;
var gems2 = [];
var see = 0;
for (var i in ptypes) {
    shop.push(new Player(65,200,false,ptypes[i],true));
    if (round(i)===0) {
        shop[i].u = true;
    }
    else {
        shop[i].u = false;
    }
}
for (var i in types) {
    gems2.push(new Gem(width-50,115+i*40,types[i],15));
}

var spike = function(x,y,t) {
    this.pos = new PVector(x,y);
    this.vel = new PVector(0,0);
    this.s = random(5,9);
    this.t = t;
    this.draw = function() {
        switch (this.t) {
            case ">":
                pushMatrix();
                translate(this.pos.x,this.pos.y);
                fill(50, 50, 50);
                noStroke();
                triangle(0,-this.s,0,this.s,this.s*1.5,0);
                popMatrix();
            break;
            case "<":
                pushMatrix();
                translate(this.pos.x,this.pos.y);
                fill(50, 50, 50);
                noStroke();
                triangle(0,-this.s,0,this.s,-this.s*1.5,0);
                popMatrix();
            break;
        }
    };
};
var star = function(y) {
    this.pos = new PVector(random(width/3,width-width/3),y);
    this.vel = new PVector(random(-3,3),0);
    this.s = random(5,9);
    this.draw = function() {
        this.pos.add(this.vel);
        pushMatrix();
        translate(this.pos.x,this.pos.y);
        rotate(frameCount*50);
        fill(50, 50, 50);
        stroke(255,255,255);
        strokeWeight(1);
        rectMode(CENTER);
        rect(0,0,(round(this.s/1.5)%4)*2,(round(this.s/1.5)%4)*2,-4);
        popMatrix();
        if (this.pos.x>width-width/3) {
            this.vel.x = -3;
        }
        if (this.pos.x<width/3) {
            this.vel.x = 3;
        }
    };
};

var powerUp = function(x,y) {
    this.ts = ["gems","bullet","sheild"];
    this.t = this.ts[floor(random(this.ts.length-0.1))];
    this.p = new PVector(x,y);
    this.v = new PVector(0,0);
    this.s = 13;
    this.ti = 30;
    this.collecting = false;
    this.draw = function() {
        pushMatrix();
        translate(this.p.x,this.p.y);
        noStroke();
        fill(59, 199, 12);
        ellipse(0,0,this.s*1.5,this.s*1.5);
        fill(255,255,255);
        textSize(this.s*1.5-5);
        text("?",0,0);
        strokeWeight(2);
        noFill();
        for (var i = 0; i<3; i++) {
            stroke(255,255,255,i*70);
            arc(0,0,this.s*1.5-4,this.s*1.5-4,-90-i*10,i*10);
        }
        popMatrix();
    };
    this.update = function() {
        this.p.add(this.v);
        this.v.limit(5);
    };
};

var hows = [];
hows.push(new spike(0,0,">"),new spike(0,0,"<"),new star(200));
for (var i in types) {
    hows.push(new Gem(45+i*80,300,types[i],20));
}

var spikes = [];

var InfiniteLevel = function(h) {
    if (h===true && homePlayer.v.y!==0 || h===false && player.v.y!==0) {
        if ((frameCount)%30===0) {
            spikes.push(new Spike());
        }
        if (frameCount%500===0) {
            gems.push(new Gem(random(width/3,width-width/3),random(-40,-10),types[floor(random(types.length))],10));
        }
        if (frameCount%720===0) {
            gems.push(new powerUp(random(width/3,width-width/3),-10));
        }
    }
    fill(50, 50, 50);
    noStroke();
    rectMode(CORNER);
    rect(0,0,width/3,height);
    rect(width,0,-width/3,height);
    for (var i in spikes) {
        spikes[i].draw();
        if (!h) {
            spikes[i].pos.y-=player.vel.y;
        }
        if (h) {
            spikes[i].pos.y-=homePlayer.vel.y;
        }
        if (spikes[i].pos.y>height+10) {
            spikes.splice(i,1);
        }
    }
    for (var i in gems) {
        gems[i].draw();
        gems[i].update();
        if (!h) {
            gems[i].p.y-=player.vel.y;
        }
        if (h) {
            gems[i].p.y-=homePlayer.vel.y;
        }
        if (gems[i].p.y>height+10) {
            gems.splice(i,1);
        }
    }
};

var Transition = function(pg) {
    this.pos = new PVector(-width/2,height/2);
    this.vel = new PVector(20,0);
    this.page = pg;
    this.engage = function() {
        noStroke();
        if (this.pos.x>width/2-5 && this.pos.x<width/2+5) {
            page = this.page;
        }
        rectMode(CENTER);
        fill(50, 50, 50);
        rect(this.pos.x,this.pos.y,width,height);
        this.pos.add(this.vel);
        rect(this.pos.x,this.pos.y,width,height);
        rectMode(CORNER);
    };
};
var trans = [];

var outline = function(message,x,y,textC,outlineC) {
    for (var i = 0; i<2; i++) {
        for (var j = 0; j<2; j++) {
            fill(outlineC);
            text(message,x+i*4-2,y+j*4-2);
        }
    }
    fill(textC);
    text(message,x,y);
};

var Message = function(m,tc,bc,w,h,seconds) {
    this.m = m;
    this.s = new PVector(w,h);
    this.o = true;
    this.p = new PVector(width/2,height+this.s.y/2);
    this.v = new PVector(0,-3);
    this.tc = tc;
    this.bc = bc;
    this.pt = [];
    this.t = 0;
    this.et = seconds*50;
    this.splice = false;
    this.draw = function() {
        this.p.add(this.v);
        if (this.o && this.p.y>=height-this.s.y/2) {
            this.v.y = -3;
        }
        else if (!this.o && this.p.y<=height+this.s.y) {
            this.v.y = 3;
        }
        else {
            this.v.y = 0;
        }
        if (!this.o && this.p.y>=height+this.s.y) {
            this.splice = true;
        }
        rectMode(CENTER);
        fill(this.bc);
        noStroke();
        rect(this.p.x,this.p.y,this.s.x,this.s.y);
        textAlign(LEFT,TOP);
        fill(this.tc);
        textSize(12.451);
        textFont(createFont("Courier New"));
        text(this.m,this.p.x-this.s.x/2+5,this.p.y-this.s.y/2+5,this.s.x-40,this.s.y);
        textAlign(CENTER,CENTER);
        fill(0);
        if (mouseX>(this.p.x+this.s.x/2-15)-7 && mouseX<(this.p.x+this.s.x/2-15)+7 &&
        mouseY>(this.p.y-this.s.y/2+15)-7 && mouseY<(this.p.y-this.s.y/2+15)+7) {
            cursor(HAND);
        }
        text("✖",this.p.x+this.s.x/2-15,this.p.y-this.s.y/2+15);
        if (mouseIsPressed && mouseX>(this.p.x+this.s.x/2-15)-7 && mouseX<(this.p.x+this.s.x/2-15)+7 && mouseY>(this.p.y-this.s.y/2+15)-7 && mouseY<(this.p.y-this.s.y/2+15)+7) {
            this.o = false;
        }
        this.t++;
        if (this.t>this.et) {
            this.o = false;
        }
    };
};
var messages = [];

var t = 0;

var go = false;

var one = 0;

var Button = function(x,y,c,t,w) {
    this.pos = new PVector(x,y);
    this.color = c;
    this.text = t;
    this.textSize = 15;
    this.inSide = false;
    this.BoxWidth = this.text.length*(this.textSize/1.5)+10;
    this.w=w;
    if (w>=0 && w<=width) {
        this.BoxWidth=this.w;
    }
    this.update = function() {
        if (mouseX>this.pos.x-this.BoxWidth/1.8 && mouseX<this.pos.x+this.BoxWidth/1.8 && mouseY>this.pos.y-this.textSize && mouseY<this.pos.y+this.textSize) {
            cursor(HAND);
            this.color = color(220, 220, 220);
            this.inSide = true;
        }
        else {
            this.inSide = false;
            this.color = c;
        }
    };
    this.draw = function() {
        pushMatrix();
        translate(this.pos.x,this.pos.y);
        fill(this.color);
        stroke(0, 0, 0);
        strokeWeight(2);
        rectMode(CENTER);
        rect(0,0,this.BoxWidth,this.textSize*2,10);
        rectMode(CORNER);
        fill(0, 0, 0);
        textAlign(CENTER,CENTER);
        textSize(this.textSize);
        text(this.text,0,0);
        popMatrix();
    };
};

var Shop = new Button(65,height/2+30,color(255, 255, 255),"",80);
}

//Logo
{
var game = "Switch";
textAlign(CENTER,CENTER);
rectMode(CENTER);
var name = [
    "J",
    "A",
    "Y",
    "C",
    "U",
    "B",
    "E"
];
var colors = [
    color(255, 255, 0),
    color(73, 173, 48),
    color(17, 0, 255),
    color(255, 162, 0)
];
var color1 = [
    color(255, 255, 125),
    color(113, 176, 95),
    color(136, 127, 255),
    color(255, 206, 122)
];
var name1Pos = 360;
var name1Change = 2;
var name2Pos = -285;
var name2Change = 2.5;
var a = 0;
var aChange = 2;
var s = 200;
var sChange = 2/3;
var my_Logo = function(x,y) {
    textFont(createFont(""));
    rectMode(CENTER);
    background(0, 0, 0);
    pushMatrix();
    translate(x,y);
    scale(0.4,0.45);
    textSize(100);
    strokeWeight(5);
    for (var i = 0; i<3; i++) {
        rotate(120);
        stroke(colors[i]);
        fill(color1[i]);
        quad(0,-4*s,80*s,-50*s,0,-90*s,-80*s,-50*s);
    }
    for (var i = 0; i<3; i++) {
        fill(colors[i]);
        text(name[i], i*60-name1Pos, -120);
    }
    for (var i = 0; i<4; i++) {
        fill(colors[i]);
        text(name[i+3], i*70-name2Pos, 120);
    }
    stroke(0);
    noFill();
    strokeWeight(350);
    rect(0,0,width+300,height+300);
    fill(255,255,0,a);
    textSize(100);
    text("Presents...",0,-height+80);
    name1Pos-=name1Change;
    if (name1Pos<60) {
        name1Change=0;
    }
    name2Pos+=name2Change;
    if (name2Pos>100) {
        name2Change=0;
    }
    s-=sChange;
    if (s<3.5 && s>2/3) {
        sChange=2/30;
    }
    if (s<=2/3) {
        s=2/3;
        a+=aChange;
    }
    if (a>300) {
        fill(158, 158, 158);
        textSize(130);
        textFont(createFont(""));
        textFont(createFont("D3 Archism"));
        text(game,0,height-80);
        textFont(createFont(""));
    }
    if (a>500) {
        trans.push(new Transition("home"));
        a=0;
    }
    popMatrix();
};
}

draw = function() {
    //frameRate(1200);
    var gravity1 = new PVector(0,0.5);
    if (page==="logo") {
        cursor("none");
        my_Logo(width/2,height/2);
        mouseClicked = function() {
            trans.push(new Transition("home"));
        };
    }
    if (page==="home") {
        cursor(ARROW);
        textAlign(CENTER,CENTER);
        fill(0, 140, 255, 150);
        noStroke();
        rectMode(CORNER);
        rect(0,0,width,height);
        
        InfiniteLevel(true);
        homePlayer.draw();
        homePlayer.update(spikes);
        homePlayer.collide(spikes);
        homePlayer.applyGravity(gravity1);
        if (homePlayer.dead && homePlayer.ps[0].y>height) {
            if (computerScore) {
                println(round(homePlayer.score));
            }
            homePlayer.score = 0;
            htype++;
            for (var i in spikes) {
                spikes.splice(i,spikes.length);
            }
            for (var i in gems) {
                gems.splice(i,gems.length);
            }
            homePlayer.vel.y = homePlayer.returnVel;
            homePlayer.pos.x = width/2;
            for (var i in homePlayer.ps) {
                homePlayer.ps[i].x = homePlayer.ss[i].x;
                homePlayer.ps[i].y = homePlayer.ss[i].y;
                homePlayer.vs[i] = new PVector(random(-3,3),random(-8,-5));
            }
            homePlayer.dead = false;
        }
        
        textFont(createFont(""));
        textFont(createFont("D3 Archism"));
        fill(255,255,255);
        textSize(100);
        text(game,width/2,50);
        textFont(createFont(""));
        textSize(30);
        if ((mouseX>width/2-30 && mouseX<width/2+30) &&
        (mouseY>height-60 && mouseY<height-40)){
            pushMatrix();
            translate(width/2,height-50);
            rotate(cos(one)*90-90);
            scale(cos(one*3),sin(one));
            text("Infinity",0,0);
            popMatrix();
            one++;
        }
        else {
            one = 0;
            text("Infinity",width/2,height-50);
        }
        
        textSize(30);
        fill(255, 255, 255);
        if ((mouseX>width/6-50 && mouseX<width/6+50) &&
        (mouseY>height/2-15 && mouseY<height/2+10)){
            textSize(35);
            fill(100,100,100);
        }
        text("Scores",width/6,height/2);
        
        textSize(30);
        fill(255, 255, 255);
        if ((mouseX>width-width/6-50 && mouseX<width-width/6+50) &&
        (mouseY>height/2-30 && mouseY<height/2+25)){
            textSize(35);
            fill(100,100,100);
        }
        text("How to\nPlay",width-width/6,height/2);
        
        textSize(30);
        fill(255,255,255);
        if ((mouseX>width-width/6-45 && mouseX<width-width/6+45) &&
        (mouseY>300-15 && mouseY<300+15)){
            textSize(35);
            fill(100,100,100);
        }
        text("Shop",width-width/6,300);
        
        textSize(30);
        fill(255, 255, 255);
        if ((mouseX>width/6-50 && mouseX<width/6+50) &&
        (mouseY>300-15 && mouseY<300+15)){
            textSize(35);
            fill(100,100,100);
        }
        text("Votes",width/6,300);
        
        mouseClicked = function() {
            if (mouseX>width/2-30 && mouseX<width/2+30 && 
            mouseY>height-60 && mouseY<height-40) {
                gems = [];
                spikes = [];
                trans.push(new Transition("game"));
            }
            if ((mouseX>width/6-50 && mouseX<width/6+50) &&
            (mouseY>height/2-15 && mouseY<height/2+10)){
                trans.push(new Transition("scores"));
            }
            if ((mouseX>width-width/6-50 && mouseX<width-width/6+50) &&
            (mouseY>height/2-30 && mouseY<height/2+25)){
                trans.push(new Transition("how"));
            }
            if ((mouseX>width-width/6-45 && mouseX<width-width/6+45) &&
            (mouseY>300-15 && mouseY<300+15)){
                trans.push(new Transition("shop"));
            }
            if ((mouseX>width/6-50 && mouseX<width/6+50) &&
            (mouseY>300-15 && mouseY<300+15)){
                trans.push(new Transition("votes"));
            }
        };
    }
    if (page==="how") {
        cursor(ARROW);
        textAlign(CENTER,CENTER);
        fill(0, 140, 255, 150);
        noStroke();
        rectMode(CORNER);
        rect(0,0,width,height);
        
        InfiniteLevel(true);
        homePlayer.draw();
        homePlayer.update(spikes);
        homePlayer.collide(spikes);
        
        homePlayer.applyGravity(gravity1);
        if (homePlayer.dead && homePlayer.ps[0].y>height) {htype++;
            for (var i in spikes) {
                spikes.splice(i,spikes.length);
            }
            for (var i in gems) {
                gems.splice(i,gems.length);
            }
            homePlayer.vel.y = homePlayer.returnVel;
            homePlayer.pos.x = width/2;
            for (var i in homePlayer.ps) {
                homePlayer.ps[i].x = homePlayer.ss[i].x;
                homePlayer.ps[i].y = homePlayer.ss[i].y;
                homePlayer.vs[i] = new PVector(random(-3,3),random(-8,-5));
            }
            homePlayer.dead = false;
        }
        
        fill(0,0,0,100);
        rect(width/2,height/2,width,height);
        
        textSize(50);
        fill(255,255,255);
        textFont(createFont("D3 Archism"));
        text("How to Play",width/2,50);
        textFont(createFont(""));
        
        strokeWeight(1);
        for (var i in hows) {
            hows[i].draw();
            if (i<=2) {
                hows[i].pos.x = i*40+width/3+20;
                hows[i].pos.y = 200;
                hows[i].s = 7;
                hows[i].vel.x = 0;
            }
            hows[2].s = 10;
            if (i>1 && i<=2) {
                noFill();
                stroke(255,255,255);
                rect(hows[i].pos.x,hows[i].pos.y,24,24);
            }
        }
        
        noFill();
        stroke(255,255,255);
        rect((hows[0].pos.x+hows[1].pos.x)/2,200,dist(hows[0].pos.x,0,hows[1].pos.x,0)+20,20);
        rect((hows[0].pos.x+hows[2].pos.x)/2,200,dist(hows[0].pos.x,0,hows[2].pos.x,0)+30,35);
        rect((hows[3].p.x+hows[7].p.x)/2,300,dist(hows[3].p.x,0,hows[7].p.x,0)+50,65);
        strokeWeight(2);
        stroke(0, 255, 0);
        line((hows[0].pos.x+hows[1].pos.x)/2,190,
             (hows[0].pos.x+hows[1].pos.x)/2-60,170);
        fill(255,255,255);
        textSize(15);
        text("Spikes",(hows[0].pos.x+hows[1].pos.x)/2-65,160);
        
        text("Use left & right arrow keys or click to switch sides. Collect gems to buy different players with different abilities!",5,-90,width-10,height);
        
        strokeWeight(2);
        stroke(0, 255, 0);
        line((hows[0].pos.x+hows[2].pos.x)/2,183,
             (hows[0].pos.x+hows[2].pos.x)/2+15,170);
        fill(255,255,255);
        text("Avoid!",(hows[0].pos.x+hows[2].pos.x)/2+15,160);
        
        line((hows[0].pos.x+hows[2].pos.x)/2,183,
             (hows[0].pos.x+hows[2].pos.x)/2+15,170);
        text("These are gems, you want to collect them",width/2,345);
        
        textFont(createFont(""));
        textSize(20);
        fill(255,255,255);
        if (mouseX>width/2-25 && mouseX<width/2+25 && mouseY>height-35 && mouseY<height-5)
        {
            textSize(25);
            cursor(HAND);
        }
        text("Back",width/2,height-20);
        mouseClicked = function() {
            if ((mouseX>width/2-25 && mouseX<width/2+25) &&
            (mouseY>height-35 && mouseY<height-5)) {
                trans.push(new Transition("home"));
            }
        };
    }
    if (page==="shop") {
        cursor(ARROW);
        textAlign(CENTER,CENTER);
        fill(0, 140, 255, 150);
        noStroke();
        rectMode(CORNER);
        rect(0,0,width,height);
        
        InfiniteLevel(true);
        homePlayer.draw();
        homePlayer.update(spikes);
        homePlayer.collide(spikes);
        
        homePlayer.applyGravity(gravity1);
        if (homePlayer.dead && homePlayer.ps[0].y>height) {htype++;
            for (var i in spikes) {
                spikes.splice(i,spikes.length);
            }
            for (var i in gems) {
                gems.splice(i,gems.length);
            }
            homePlayer.vel.y = homePlayer.returnVel;
            homePlayer.pos.x = width/2;
            for (var i in homePlayer.ps) {
                homePlayer.ps[i].x = homePlayer.ss[i].x;
                homePlayer.ps[i].y = homePlayer.ss[i].y;
                homePlayer.vs[i] = new PVector(random(-3,3),random(-8,-5));
            }
            homePlayer.dead = false;
        }
        
        textFont(createFont(""));
        textSize(20);
        textAlign(LEFT,CENTER);
        var myGems = [
            player.emeralds,
            player.rubies,
            player.tris,
            player.diamonds,
            player.blackDiamonds
        ];
        textAlign(CENTER,CENTER);
        textSize(15);
        fill(255);
        text("Total Money: $"+player.total,65,height/2+100);
        
        shop[see].draw();
        fill(255,255,255);
        text("Cost\n$"+shop[see].cost,65,height/2-35);
        if (shop[see].u===false) {
            Shop.text = "Buy";
        }
        else if (shop[see].u===true && shop[see].t!==player.t) {
            Shop.text = "Equip";
        }
        else {
            Shop.text = "Equipped";
        }
        Shop.draw();
        if (shop[see].t!==player.t && shop[see].u!==true ||
        shop[see].t!==player.t && shop[see].u===true) {
            Shop.update();
        }
        
        textAlign(CENTER,CENTER);
        textFont(createFont(""));
        textFont(createFont("D3 Archism"));
        fill(255,255,255);
        textSize(100);
        text("Shop",width/2,40);
        
        textFont(createFont(""));
        textSize(20);
        fill(255,255,255);
        if (mouseX>width/2-25 && mouseX<width/2+25 && mouseY>height-35 && mouseY<height-5)
        {
            textSize(25);
            cursor(HAND);
        }
        text("Back",width/2,height-20);
        mouseClicked = function() {
            if ((mouseX>width/2-25 && mouseX<width/2+25) &&
            (mouseY>height-35 && mouseY<height-5)) {
                trans.push(new Transition("home"));
            }
            if (Shop.inSide) {
                if (shop[see].u===false) {
                    if (player.total>=shop[see].cost) {
                        player.total -= shop[see].cost;
                        shop[see].u = true;
                        player.t = shop[see].t;
                        messages.push(new Message("Transaction successful",color(0, 0, 0),color(140, 140, 140),300,25,2));
                    }
                    else {
                        if (messages.length<1) {
                            messages.push(new Message("Sorry you don't have enough to buy this one! :/",color(0, 0, 0),color(140, 140, 140),300,38,5));
                        }
                    }
                }
                if (shop[see].u===true && shop[see].t!==player.t) {
                    player.t = shop[see].t;
                }
            }
        };
    }
    if (page==="scores") {
        cursor(ARROW);
        textAlign(CENTER,CENTER);
        fill(0, 140, 255, 150);
        noStroke();
        rectMode(CORNER);
        rect(0,0,width,height);
        
        textAlign(LEFT,CENTER);
        textFont(createFont(""));
        var _ = 35;
        for (var i = scores.length-1; i>-1; i--) {
            textSize(17);
            fill(255, 0, 0);
            image(scores[i][2],width/7,150+(scores.length-i-1)*_+sy,30,30);
            text((scores.length-i)+". "+scores[i][1]+" got "+scores[i][0],width/7+18,150+(scores.length-i-1)*_+sy);
        }
        if (mouseIsPressed && sy<=0) {
            sy+=mouseY-pmouseY;
        }
        if (sy>0) {
            sy = 0;
        }
        if (sy<-scores.length*(_-3)) {
            sy = -scores.length*(_-3);
        }
        
        textAlign(CENTER,CENTER);
        pushMatrix();
        textSize(15);
        translate(width-10,height/2+30);
        rotate(-90);
        text("Click and drag to scroll",0,0);
        popMatrix();
        
        for (var i = 0; i<15; i++) {
            rectMode(CENTER);
            fill(0, 140, 255, 50);
            rect(width/2,50,width,100+i*3);
            rect(width/2,height-20,width,40+i*3);
        }
        textFont(createFont(""));
        textFont(createFont("D3 Archism"));
        fill(255,255,255);
        textSize(100);
        text("Scores",width/2,50);
        textSize(15);
        if (who.length<2) {
            text("Your playing as a guest",width/2,100);
        }
        else {
            text("Your playing as "+who,width/2,100);
        }
        textFont(createFont(""));
        textSize(20);
        fill(0, 0, 0);
        if (mouseX>20-12 && mouseX<20+12 &&
        mouseY>height/2-100 && mouseY<height/2+100) {
            fill(100, 100, 100);
            textSize(25);
        }
        pushMatrix();
        translate(20,height/2);
        rotate(90);
        text("Show My Score",0,0);
        popMatrix();
        textSize(20);
        fill(255,255,255);
        if (mouseX>width/2-25 && mouseX<width/2+25 && mouseY>height-35 && mouseY<height-5)
        {
            textSize(25);
            cursor(HAND);
        }
        text("Back",width/2,height-20);
        mouseClicked = function() {
            if ((mouseX>width/2-25 && mouseX<width/2+25) &&
            (mouseY>height-35 && mouseY<height-5)) {
                player.prev = player.score; player.score = 0;
                trans.push(new Transition("home"));
            }
            if (mouseX>20-12 && mouseX<20+12 &&
            mouseY>height/2-100 && mouseY<height/2+100 && player.score!==player.high) {
                if (who.length<2) {
                    scores.push([player.high,"You"]);
                    println("Make a spin-off with your score showing (even if it is small) then paste the link to it in a comment below. To have your score on the score board.");
                    who = "You";
                    quickSort(scores,0,scores.length-1);
                }
                else if (who!=="") {
                    for (var i in scores) {
                        if (player.high>scores[i][0] && scores[i][1]===who) {
                            scores[i][0] = player.high;
                        }
                    }
                    quickSort(scores,0,scores.length-1);
                    println("Make a spin-off with your score showing (even if it is small) then paste the link to it in a comment below. To have your score on the score board.");
                }
                else {
                    if (player.high!==0) {
                        scores.push([player.high,who]);
                        println("Make a spin-off with your score showing (even if it is small) then paste the link to it in a comment below. To have your score on the score board.");
                        quickSort(scores,0,scores.length-1);
                    }
                }
                player.score = player.high;
            }
        };
    }
    if (page==="game") {
        cursor(ARROW);
        textAlign(CENTER,CENTER);
        fill(0, 140, 255, 150);
        noStroke();
        rectMode(CORNER);
        rect(0,0,width,height);
        
        if (go) {
            InfiniteLevel(false);
            player.draw();
            player.update();
            player.collide(spikes);
            for (var i in gems) {
                if (dist(gems[i].p.x,gems[i].p.y,player.pos.x,player.pos.y)<(gems[i].s+5)) {
                    if (gems[i].t.toLowerCase()==="emerald") {
                        player.total += gems[i].c;
                        player.emeralds++;
                        gems.splice(i,1);
                    }
                    else if (gems[i].t.toLowerCase()==="ruby") {
                        player.total += gems[i].c;
                        player.rubies++;
                        gems.splice(i,1);
                    }
                    else if (gems[i].t.toLowerCase()==="tri-emerald") {
                        player.total += gems[i].c;
                        player.tris++;
                        gems.splice(i,1);
                    }
                    else if (gems[i].t.toLowerCase()==="diamond") {
                        player.total += gems[i].c;
                        player.diamonds++;
                        gems.splice(i,1);
                    }
                    else if (gems[i].t.toLowerCase()==="black-diamond") {
                        player.total += gems[i].c;
                        player.blackDiamonds++;
                        gems.splice(i,1);
                    }
                    else if (gems[i].t.toLowerCase()==="gems") {
                        gems.splice(i,1);
                        player.gemMagnet = true;
                    }
                    else if (gems[i].t.toLowerCase()==="bullet") {
                        gems.splice(i,1);
                        player.bullet = true;
                    }
                    else if (gems[i].t.toLowerCase()==="sheild") {
                        gems.splice(i,1);
                        player.sheild = true;
                    }
                }
            }
            for (var j in player.v) {
                for (var i in gems) {
                    if (dist(gems[i].p.x,gems[i].p.y,player.v[i].x,player.v[i].y)<(gems[i].s+5)) {
                        if (player.t.toLowerCase()==="earth" || player.sheild) {
                            if (gems[i].t.toLowerCase()==="emerald") {
                                player.total += gems[i].c;
                                player.emeralds++;
                                gems.splice(i,1);
                            }
                            else if (gems[i].t.toLowerCase()==="ruby") {
                                player.total += gems[i].c;
                                player.rubies++;
                                gems.splice(i,1);
                            }
                            else if (gems[i].t.toLowerCase()==="tri-emerald") {
                                player.total += gems[i].c;
                                player.tris++;
                                gems.splice(i,1);
                            }
                            else if (gems[i].t.toLowerCase()==="diamond") {
                                player.total += gems[i].c;
                                player.diamonds++;
                                gems.splice(i,1);
                            }
                            else if (gems[i].t.toLowerCase()==="black-diamond") {
                                player.total += gems[i].c;
                                player.blackDiamonds++;
                                gems.splice(i,1);
                            }
                            else if (gems[i].t.toLowerCase()==="gems") {
                                gems.splice(i,1);
                                player.gemMagnet = true;
                            }
                            else if (gems[i].t.toLowerCase()==="bullet") {
                                gems.splice(i,1);
                                player.bullet = true;
                            }
                            else if (gems[i].t.toLowerCase()==="sheild") {
                                gems.splice(i,1);
                                player.sheild = true;
                            }
                        }
                    }
                }
            }
            for (var j in player.v1) {
                for (var i in gems) {
                    if (dist(gems[i].p.x,gems[i].p.y,player.v1[i].x,player.v1[i].y)<(gems[i].s+5)) {
                        if (player.t.toLowerCase()==="earth" || player.sheild) {
                            if (gems[i].t.toLowerCase()==="emerald") {
                                player.total += gems[i].c;
                                player.emeralds++;
                                gems.splice(i,1);
                            }
                            else if (gems[i].t.toLowerCase()==="ruby") {
                                player.total += gems[i].c;
                                player.rubies++;
                                gems.splice(i,1);
                            }
                            else if (gems[i].t.toLowerCase()==="tri-emerald") {
                                player.total += gems[i].c;
                                player.tris++;
                                gems.splice(i,1);
                            }
                            else if (gems[i].t.toLowerCase()==="diamond") {
                                player.total += gems[i].c;
                                player.diamonds++;
                                gems.splice(i,1);
                            }
                            else if (gems[i].t.toLowerCase()==="black-diamond") {
                                player.total += gems[i].c;
                                player.blackDiamonds++;
                                gems.splice(i,1);
                            }
                            else if (gems[i].t.toLowerCase()==="gems") {
                                gems.splice(i,1);
                                player.gemMagnet = true;
                            }
                            else if (gems[i].t.toLowerCase()==="bullet") {
                                gems.splice(i,1);
                                player.bullet = true;
                            }
                            else if (gems[i].t.toLowerCase()==="sheild") {
                                gems.splice(i,1);
                                player.sheild = true;
                            }
                        }
                    }
                }
            }
            player.applyGravity(gravity1);
        }
        
        fill(255, 255, 255);
        textSize(20);
        textFont(createFont(""));
        textAlign(LEFT,TOP);
        text("Score: "+abs(floor(player.score))+"\nPrevious: "+floor(player.prev),10,10);
        textAlign(RIGHT,CENTER);
        text("High: "+abs(floor(player.high)),width-10,20);
        textAlign(CENTER,CENTER);
        textSize(15);
        fill(255);
        text("Total Money: $"+player.total,65,height/2+100);
        
        if (!go) {
            textSize(25);
            if (mouseX>width/2-40 && mouseX<width/2+40 && mouseY>height/1.9-20 && mouseY<height/1.9+20) {
                textSize(30);
            }
            outline("Start!",width/2,height/1.9,color(0, 0, 0),color(170,170,170));
        }
        
        if (round(abs(player.score))===round(abs(player.high))+1 && !player.dead && player.high!==0 && messages.length<1) {
            messages.push(new Message("Hey! You just beat your previous highscore! Keep going!",color(0, 0, 0),color(140, 140, 140),300,40,2));
        }
        
        textFont(createFont(""));
        textSize(20);
        fill(255,255,255);
        if (mouseX>width/2-25 && mouseX<width/2+25 && mouseY>height-35 && mouseY<height-5)
        {
            textSize(25);
            cursor(HAND);
        }
        text("Back",width/2,height-20);
        
        if (player.dead) {
            if (t<200) {
                t+=2;
            }
            rectMode(CORNER);
            fill(255,255,255,t);
            rect(0,0,width,height);
            textSize(25);
            outline("You Died!",width/2,height/4,color(0, 0, 0, t),color(170,170,170, t));
            
            textSize(25);
            if (mouseX>width/2-100 && mouseX<width/2+100 && mouseY>height/1.4-20 && mouseY<height/1.4+20) {
                textSize(30);
            }
            outline("Play Again!",width/2,height/1.4,color(0, 0, 0, t),color(170,170,170, t));
            
            textSize(25);
            if (mouseX>width/2-40 && mouseX<width/2+40 && mouseY>height/1.9-20 && mouseY<height/1.9+20) {
                textSize(30);
            }
            outline("Home",width/2,height/1.9,color(0, 0, 0, t),color(170,170,170, t));
        }
        mouseClicked = function() {
            if (mouseX>width/2-40 && mouseX<width/2+40 &&
            mouseY>height/1.9-20 && mouseY<height/1.9+20) {
                go = true;
            }
            if (player.dead && t>=190 && mouseX>width/2-100 && mouseX<width/2+100 &&
            mouseY>height/1.4-20 && mouseY<height/1.4+20) {
                for (var i in spikes) {
                    spikes.splice(i,spikes.length);
                }
                for (var i in gems) {
                    gems.splice(i,gems.length);
                }
                player.pos.x = width/2;
                player.vel.x = 0;
                player.right = true;
                player.left = false;
                for (var i in player.ps) {
                    player.ps[i].x = player.ss[i].x;
                    player.ps[i].y = player.ss[i].y;
                    player.vs[i] = new PVector(random(-3,3),random(-8,-5));
                }
                t = 0;
                player.prev = player.score; player.score = 0;
                player.vel.y = player.returnVel;
                player.dead = false;
            }
            if (player.dead && t>=190 && mouseX>width/2-40 && mouseX<width/2+40 &&
            mouseY>height/1.9-20 && mouseY<height/1.9+20) {
                for (var i in spikes) {
                    spikes.splice(i,spikes.length);
                }
                for (var i in gems) {
                    gems.splice(i,gems.length);
                }
                trans.push(new Transition("home"));
            }
            if ((mouseX>width/2-25 && mouseX<width/2+25) &&
            (mouseY>height-35 && mouseY<height-5 && !player.dead)) {
                if (round(abs(player.score))>=player.high) {
                    player.high = player.score;
                }
                player.prev = player.score; player.score = 0;
                trans.push(new Transition("home"));
            }
        };
    }
    if (page==="votes") {
        cursor(ARROW);
        textAlign(CENTER,CENTER);
        fill(0, 140, 255, 150);
        noStroke();
        rectMode(CORNER);
        rect(0,0,width,height);
        
        textSize(30);
        fill(0);
        var x1 = width/2-100;
        var x2 = width/2+100;
        text("Bar",x1,100);
        text("Line",x2,100);
        
        if (mouseX<x1+60 && mouseX>x1-60 && mouseY<140 && mouseY>60) {
            type = "bar";
        }
        if (mouseX<x2+60 && mouseX>x2-60 && mouseY<140 && mouseY>60) {
            type = "line";
        }
        
        stroke(0);
        strokeWeight(1);
        for (var i = -2; i<8; i++) {
            stroke(0);
            line(50+i*70+Cx%70,150,50+i*70+Cx%70,height-60);
            line(0,height-60-(i+2)*20,width,height-60-(i+2)*20);
        }
        line(0,150,width,150);
        line(0,height-60,width,height-60);
        for (var i = 0; i<votes.length; i++) {
            fill(255,0,0);
            textSize(14);
            textAlign(CENTER,CENTER);
            text(votes[i][0],50+i*70+Cx,height-50);
            text(votes[i][1]+" votes",50+i*70+Cx,150-8);
            if (mouseY>150 && mouseY<height-50 && mouseX>25+i*70+Cx && mouseX<75+i*70+Cx) {
                textAlign(LEFT,CENTER);
                text(votes[i][2],mouseX+15,mouseY-190,100,height);
            }
            if (type==="bar") {
                rectMode(CORNER);
                rect(50+i*70+Cx,height-60,5,-votes[i][1]/4);
            }
            if (type==="line") {
                if (i<votes.length-1) {
                    stroke(255, 0, 0);
                    line(50+i*70+Cx,height-60-votes[i][1]/4,50+(i+1)*70+Cx,height-60-votes[i+1][1]/4);
                }
            }
        }
        if (mouseY>150 && mouseY<height-50) {
            cursor("cell");
        }
        if (mouseIsPressed && mouseY>150 && mouseY<height-50) {
            cursor("all-scroll"); //Don't recognize these cursors? Go here: https://www.khanacademy.org/computer-programming/processingjs-cursor-styles/4874036493484032
            //Or go here: http://www.w3schools.com/cssref/playit.asp?filename=playcss_cursor&preval=auto
            Cx += mouseX - pmouseX;
        }
        
        textAlign(CENTER,CENTER);
        textFont(createFont(""));
        fill(255,255,255);
        textSize(50);
        text("Votes",width/2,40);
        
        textFont(createFont(""));
        textSize(20);
        fill(255,255,255);
        if (mouseX>width/2-25 && mouseX<width/2+25 && mouseY>height-35 && mouseY<height-5)
        {
            textSize(25);
            cursor(HAND);
        }
        text("Back",width/2,height-20);
        
        mouseClicked = function() {
            if (mouseX>width/2-25 && mouseX<width/2+25 &&
            mouseY>height-35 && mouseY<height-5) {
                trans.push(new Transition("home"));
            }
        };
    }
    for (var i in trans) {
        trans[i].engage();
        if (trans[i].pos.x>width*1.5) {
            trans.splice(i,1);
        }
    }
    for (var i in messages) {
        messages[i].draw();
        if (messages[i].splice) {
            messages.splice(i,1);
        }
    }
    for (var i = gems.length-1; i>-1; i--) {
        if (dist(gems[i].p.x,gems[i].p.y,homePlayer.pos.x,
        homePlayer.pos.y)<(gems[i].ti*3) && page!=="game" || gems[i].collecting===true &&
        page!=="game") {
            if (homePlayer.gemMagnet) {
                gems[i].p.x = homePlayer.pos.x+(gems[i].ti*3)*cos(abs(gems[i].ti)*15+cos(gems[i].p.x - homePlayer.pos.x));
                gems[i].p.y = homePlayer.pos.y+(gems[i].ti*3)*sin(abs(gems[i].ti)*15+sin(gems[i].p.y - homePlayer.pos.y));
                gems[i].ti -= 0.5;
                gems[i].collecting = true;
            }
        }
        if (dist(gems[i].p.x,gems[i].p.y,player.pos.x,
        player.pos.y)<(gems[i].ti*3) && page==="game" || gems[i].collecting===true &&
        page==="game") {
            if (player.gemMagnet) {
                gems[i].p.x = player.pos.x+(gems[i].ti*3)*cos(abs(gems[i].ti)*15+cos(gems[i].p.x - player.pos.x));
                gems[i].p.y = player.pos.y+(gems[i].ti*3)*sin(abs(gems[i].ti)*15+sin(player.pos.y - gems[i].p.y));
                gems[i].ti -= 0.5;
                gems[i].collecting = true;
            }
        }
        if (dist(gems[i].p.x,gems[i].p.y,homePlayer.pos.x,
        homePlayer.pos.y)<(gems[i].s+5) && page!=="game") {
            if (gems[i].t.toLowerCase()==="emerald") {
                gems.splice(i,1);
            }
            else if (gems[i].t.toLowerCase()==="ruby") {
                gems.splice(i,1);
            }
            else if (gems[i].t.toLowerCase()==="tri-emerald") {
                gems.splice(i,1);
            }
            else if (gems[i].t.toLowerCase()==="diamond") {
                gems.splice(i,1);
            }
            else if (gems[i].t.toLowerCase()==="black-diamond") {
                gems.splice(i,1);
            }
            else if (gems[i].t.toLowerCase()==="gems") {
                gems.splice(i,1);
                homePlayer.gemMagnet = true;
            }
            else if (gems[i].t.toLowerCase()==="bullet") {
                gems.splice(i,1);
                homePlayer.bullet = true;
            }
            else if (gems[i].t.toLowerCase()==="sheild") {
                gems.splice(i,1);
                homePlayer.sheild = true;
            }
        }
    }
    if (trans.length>0) {
        bts = [];
        cursor("wait");
    }
    homePlayer.t = ptypes[floor(htype%ptypes.length)];
    if (frameCount%80===0 && mouseX>width/3) {
        see ++;
        if (see>=ptypes.length) {
            see=0;
        }
    }
    for (var i in bts) {
        bts[i].draw();
        bts[i].update();
        bts[i].applyForce(gravity1);
        for (var j in spikes) {
            if (dist(bts[i].pos.x,bts[i].pos.y,
            spikes[j].pos.x,spikes[j].pos.y)<spikes[j].s*5) {
        var dir = new PVector((spikes[j].pos.x-bts[i].pos.x)/15,(spikes[j].pos.y-bts[i].pos.y)/15);
                bts[i].vel.add(dir);
                bts[i].vel.limit(3);
            }
            if (dist(bts[i].pos.x,bts[i].pos.y,
            spikes[j].pos.x,spikes[j].pos.y)<spikes[j].s*2.5) {
                bts[i].count++;
                spikes.splice(j,1);
            }
        }
    }
    for (var i in bts) {
        if (bts[i].pos.y<-30 || bts[i].pos.y>height+20) {
            bts.splice(i,1);
        }
    }
    for (var i in bts) {
        if (bts[i].count>3) {
            bts.splice(i,1);
        }
    }
};
