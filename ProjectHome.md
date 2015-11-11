Software Institute, Nanjing University Spring 2009
(March 2, 2009)
Project Software - Columns Game
Project Descriptions: (for Phase B and C)
The game Columns is rather well known, at least in its dynamic form, as TETRIS.
The player can manipulate a bar of colored squares while it drops down. Once it has
reached the playing field, points are gained and squares in the playing field disappear,
according to certain rules. This game is very exciting, as the bars will drop down
faster and faster as the game goes on. For some people it turns out to be too exciting,
as they get a nervous breakdown from playing this game. For those people the static
variant was invented. (Of course not playing at all would be a better idea. But the real
addicts get a nervous breakdown if they don’t play as well.)
Let me explain Static Columns to you. The playing field is a rectangle of width w and
height h. Initially it is empty, but after some time it may be filled with colored squares.
In the scheme below the colors are indicated with capitals. The squares are subject to
gravity: a square rests either on the floor or on another square. Repeatedly a vertical
bar (extent n, now n=1) of colored squares appears on top of the playing field, against
the left wall.
The player may manipulate this bar using (repeatedly) any of the following
commands:
Command Action
r (right) Move the bar one step to the right. This command has no effect if the bar
is already at the rightmost position of the playing field.
l (left) Move the bar one step to the left. This command has no effect if the bar
is already at the leftmost position of the playing field.
s (shift) Shift (or actually rotate) the colors in the bar. The rotation is
downwards: every color goes down one step, and the lowermost color is
put on top.
d (drop) Drop the bar. After this command, no other commands can be given for
that bar.
After the commands rrrs the situation in
the above example will be:
The drop command makes the bar going
straight down until it is stopped, either by
the floor or by a colored square.
If the playing ground is very full, or the bar is very
long it may happen that the bar is stopped before it
is fully inside the playing ground. In that case the
game is over and no other bars will be played. If
not, two things happen. First, credits are counted,
depending of the parameter l, the length of a series. Whenever l squares in the field in
a series (horizontal, vertical or diagonal) have the same color, one point is given to the
player. As indicated in the next diagram, the player receives 5 points if l=3 (the player
would receive 2 points if l=4 and 1 points if l=5).
After all squares occurring in one or more such a
series have disappeared, the following diagram is
obtained:
Now gravity takes over, and the diagram becomes:
Once again a series is found and the player obtains
one more point. The final situation is:
Using the Internet every move of every players is broadcasted all over the world.
People with beautiful graphics on their machine will be able to replay the game.
You are ask to write a program to calculate the credits.