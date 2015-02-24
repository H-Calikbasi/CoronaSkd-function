# CoronaSkd-function
I would like to call the following functions just once. After the functions is called it should disappear.  


local backgroundSpeed = 2; 
local azh = 200;
local gameSpeed = azh;


leveltime = function(self)
 if gameIsPaused then
      return;
 end     
        gameSpeed = azh + 50; 
        backgroundSpeed = 2+1;
        physics.setGravity(0, 25);
 
        local myText = display.newText( "Funkt", 100, 200, native.systemFont, 56 )
             myText:setFillColor( 100, 0, 0 )   
             transition.to( myText, { time=5000,  x= (math.random(10,340)), y= 220, fadein=50, duration=1000, alpha=1})
        local square1 = display.newCircle( math.random(0,490), 0, 15)  
             transition.to( square1, { time=500,  x= (math.random(20,290)), y= 220, fadein=50, duration=1000, alpha=1})
end
timer.performWithDelay( 3000, leveltime )
