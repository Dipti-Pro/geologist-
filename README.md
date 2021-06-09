## For solution
### in sketch.js
    plane = new Plane(600,height,1200,20)
    iron = new Iron(300,350);
    stone = new Stone(700,320,100,100);
  
    rubber=new Rubber(900,450,70);
    hammer = new Hammer(10,100);
    
### in stone.js
class Stone {
  constructor(x, y, width, height) {
    var options = {
        'restitution':0.8,
        'friction':0.9,
        'density':12
    }
    this.body = Bodies.rectangle(x, y, width, height, options);
    this.width = width;
    this.height = height;
    
    World.add(world, this.body);
  }
  display(){
    var pos =this.body.position;
    var angle = this.body.angle;
    push();
    translate(pos.x, pos.y);
    rotate(angle);
    rectMode(CENTER);
    strokeWeight(4);
    stroke("black");
    fill("black");
    rect(0, 0, this.width, this.height);
    pop();
  }
};
