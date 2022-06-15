# Marcel_Method_2022
An updated version of my marcel method for NHL projections. This version can now produce Marcels for any season dating back to 2011, it cannot go back further because
previous seasons do not include FOW/FOL/Hit/Blk counts.

This version has incorporated the techniques I have learned since trying to create the previous version. Uses hockeyref to get all of the data
required for the projections.

This new method still assumes that players will play in all 82 games of a season. While Tangotiger has discussed projecting GP, see this twitter post https://twitter.com/tangotiger/status/1511712124174798854, I'm not happy with the results that occur when using a weighted average of GP to project future GP. For that reason, I used the following fomrula: 74*.65+.2*gp.season1+.2*gp.season2. This allows for players that have typically stayed healthy to project for more GP while also not severly punishing those that had fluke long term injuries. For example, if a player had played in all 82 games in season 1 and season 2 they would project to play in 81 games. If a player missed season 2 and then played 72 games in season 1 they would project for
