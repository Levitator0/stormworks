# stormworks

So, I had incredibly bad problems living in the US, and I complained about it on the Steam forums, and Geometa
summarily banned me, called me a racist, and then days later, it occurred to them to block me from uploading
vehicles to the workshop. I'd like to keep politics out of my vehicle reposity, but I think it's important to
have the right to say that people viciously abused you if the need strikes you. It's a shame that people behave
this way, and I'm not going into it in any great detail here. This is about the Stormworks vehicles, and it's a
great game. But anyway, that's the reason I'm uploading my vehicles to Github instead of using the Steam Workshop.

# Ford Ranger
When modeling real vehicles, they tend to come out beefier, and that's probably partly because you can't spawn any object
in the game that's smaller than 1/4 cubic meter in size. So, this is a really big take on the Ford Ranger, which ends up
more resembling something like an F150, or something. I'm fond of the Ranger because the real thing has served me very well.

This one has a two-speed manual transmission with reverse and neutral. It's only 2-speed because first gear can take it
all the way up to its top speed, at the limit of the wheel traction. The second gear ends up serving as an overdrive, to
reduce the RPM and save fuel.

It has a 4wd switch, but I haven't found a reason to turn it off. Turning it on significantly increases the top speed
because the speed winds up limited by the tire traction. You can experiment to see if it's more fuel efficient in 2wd at lower
speeds due to less friction.

It is generously stocked with campaign tools and items. Seating is for a driver and up to eight passengers.

Notes on controls:
I am accustomed to using analog gamepad triggers to serve as the pedals on a vehicle, so that's how I have this set up.
Most axes idle at 0 and the extremes are -1 and +1. Triggers are different, and they sit at one extreme and go to the other
when you pull them. So, axes 5 and 6 are set up to be full-throw gamepad triggers for the brake and accelerator.

Perhaps somewhat quirkily, the clutch is analog. As far as I can tell, the gearboxes in the game are indifferent to being
shifted at maximum load. However, the analog clutch might be useful for tricky starts, where you don't want to jerk to a start,
or if there's some potential to stall. Clutch release is proportional to Axis 2 deflection from center. So, you can hold the stick up
or down to release the clutch, and then ease it back to idle to engage it, like the pedal in a real vehicle.

Aside from inventory stocks, this vehicle does not have armament. It does, however, have a trailer hitch, so you can tow whatver
artillery you could come up with. I previously made an AT field gun which is ideal for this purpose. You could also create
other towed cannons, launchers, and field artillery to pull around with it. I think there's room in the bed to mount a gun or
turret, and still seat passengers, possibly.

# Piper Saratoga
I've a added an aircraft loosely based on the Piper Saratoga, originally a large six-place GA aircraft.
It's intended both to resemble the original, and to be suitable for playing the campaign.
This one is scaled up partly because the game kind of demands it, being on a slightly different scale.
Where the original only seated six, it's common in the game to have to rescue up to eight, so
this version is then further bumped up in size slightly to seat a pilot and eight passengers.

It flies great, reaching about 150kts, and it can get up to 160 with the prop pitch pulled back for maximum RPM.
Cruise seems somewhere around 130kts, at around 82% throttle. The speed loss is pretty small,
but there's a huge fuel savings.

The nosewheel is retractable, though in my experience, retracting gear has zero effect in the game. There are
some surfaces in the game where it matters how they are facing to the point where you can almost
use them as control surfaces, but the landing gear is insignificant for drag. The retractable
nosewheel is left in for looks and for fun. On a closely related not, I wanted to implement pitch control
as a stabilator, like the real thing, but it seems that the aerodynamic simulation for voxel objects is
not detailed enough for that purpose. It is implemented to some extent, but as far as I can tell it
seems like they optimized it so that user-defined objects have a huge dead-zone, where they do nothing in a certain range,
and then all of a sudden, the drag/lift simulation kicks in and it whips the vehicle around violently.
So, if you want a control surface, you should use an object designated for that purpose instead of trying to
model a fin or airfoil yourself.

I created a fuel computer just for this guy, which I think I will begin incorporating into other designs.

The handling and performance came out much better than I expected, and this was originally going to be
a non-combatant vehicle, but the addition of armament and radar is on the potential to-do list, now.

Controls:
The only unusual controls are the toe-brakes, which expect full-throw gamepad triggers as axes, as explained
for the Ranger above. Also, because we are running out of buttons and axes, the flaps are operated by pushing
in the left stick button and simultaneously pushing the up/down axis to move the flap ('throttle') lever in the plane. That way,
you don't have to worry about accidentally bumping the flaps up and down when operating a perpendicular axis on the same stick
(rudder for me). I put throttle and and flap gauges right in the central field of view so that you can see where they are set without
having to move the view around.

UPDATE: The Saratoga is ready for playtesting.

# OH-6 Cayuse/Loach
I decided that the Cayuse would make an ideal game campaign vehicle due to its small size, low cost, versatility, and abiltiy to land anywhere.
This model came out pretty close-looking. The handling is quite difficult, and it requires persistent, deliberate, and precise tension on the sticks to push it past the air resistance because it will whip around and sideslip easily, so, you have to heave it against the airflow without overcontrolling and making the problem worse. I don't think this problem can be much avoided without relying on the gryros, and they are going to produce stable but very sluggish and pokey handling that I'm not interested in. It handles quite acceptably once you get used to really paying attention to the stick positions, and you can't just knock the sticks around to full throw and expect to keep control.

It's pretty much designed to operate at 2000 turbine RPM right now. I need to find out what that is at the rotor head. As I said, it's a tiny helicopter, so it winds up with a pretty small flight envelope. If you reved it higher, it would wreck your fuel economy, and if you rev it lower, the cyclic is ineffective.

It's almost done, and I just need to finish the main display so that is shows the engine status, air speed, and altitude. Currently concerned with improving the fuel economy, as it seems to burn about 250L per 5km. There might be something that can be done with the rotor gearing.






