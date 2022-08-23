# Day 23

Today, I started working on another App for my team.

At some point, I ran into a RenderFlex Overflow Exception error and as I'd usually do, Wrap my entire widget tree withinn my Scaffold's body with a SingleChildScrollView BUT I kept on getting the same Exception error.

After hours of research and debugging, I found out that the problem was caused by the fact that I used a Flexible Widget as a Child of a ListTile Widget which was wrong because a Flexible() Widget can only be a child of a Flex(), Row() or Column() Widget.

The solution was to simply wrap the Flexible Widget in a Row Widget since I was using the Flexible Widget to make the Text Widget wrap it's content in case it's too long which was in the ListTile widget.

I was able to learn a lot about Parent and Child Widgets in Flutter and how to use them properly.
