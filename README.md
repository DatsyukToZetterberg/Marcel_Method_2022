# Marcel_Method_2022

An updated version of my marcel method for NHL projections. This version can now produce Marcels for any season dating back to 2011, it cannot go back further because
previous seasons do not include FOW/FOL/Hit/Blk counts. If one wanted to go back further you could remove those categories and the code should still work.

This version has incorporated the techniques I have learned since the previous version was created. This version uses hockeyreference to get all of the data
required for the projections. The biggest changes come in the form of a revamped method for projecting TOI, a different weighting method - a 6-3-1 method was used, and a GP projection method was created.

This new method allows for the GP projection of most players to be created. Tangotiger has discussed projecting GP, see this [blog post](http://tangotiger.net/NHL_forecast.html). I'm not certain that I agree with the idea that a cap of 76 GP is appropriate. Thus my method for projecting GP diverges from what Tango discussed in the post.

The approach taken for the GP calculation was to separate players into either "depth" or "non depth" roles based on their projected toi stat, 13.25 minutes per game for Forwards and 17.50 for Defenceman. These players would then have their projected GP stats regressed towards either 40, 74, or 76 based on their previous 2 seasons of GP data. These numbers were chosen arbitrarily so there may be a more efficient set; however, I feel as though they do create an accurate representation of a player's most likely GP. The one issue that comes from this method is the abrupt end to each set of players. Ideally there would be a smooth transition from 1 set of players to the next, but 2 distinct distributions arrive from this method of binning.

Future versions may be focused on correcting these binning issues, but for now I am content with the overall product. For a more through breakdown of the Hockey Marcels see this [medium post](https://medium.com/@datsyuktozetterbergb/the-hockey-marcels-version-2-0-2ef1b974ea88)
