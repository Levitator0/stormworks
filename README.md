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

4-speed manual transmission with reverse and neutral.

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
nosewheel is left in for looks and for fun. On a closely related note, I wanted to implement pitch control
as a stabilator, like the real thing, but it seems that the aerodynamic simulation for voxel objects is
not detailed enough for that purpose. It is implemented to some extent, but as far as I can tell it
seems like they optimized it so that user-defined objects have a huge dead-zone, where they do nothing in a certain range,
and then all of a sudden, the drag/lift simulation kicks in and it whips the vehicle around violently.
So, if you want a control surface, you should use an object designated for that purpose instead of trying to
model a fin or airfoil yourself.

I created a fuel computer just for this guy, which I think I will begin incorporating into other designs.

The handling and performance came out much better than I expected, and this was originally going to be
a non-combatant vehicle, but the addition of armament and radar is on the potential to-do list, now.

I added a V2 variant of the Saratoga which replaces the standard medium engine with a modular engine which is less
powerful and more marginal for cooling, but far more efficient. It also adds a hydrofoil and floats near the nose,
which make the plane amphibious and permit takeoffs from the water.

Added an amphibious tanker variant with twelve internal large tanks. It handles quite poorly, and it's probably a good idea
do ditch the cannons and ammo when doing supply or trade runs. Takeoff from the water is doable, but tricky.
Come up to maximum speed at about 20% prop pitch, skimming the water, with the nose up just enough to keep the prop 
out of the water, storing momentum in the propeller. Then, jam the pitch lever forward to convert the energy stored
in the prop into thrust, and you have just enough power to pull free from the drag in the water, and take off.

Controls:
The only unusual controls are the toe-brakes, which expect full-throw gamepad triggers as axes, as explained
for the Ranger above. Also, because we are running out of buttons and axes, the flaps are operated by pushing
in the left stick button and simultaneously pushing the up/down axis to move the flap ('throttle') lever in the plane. That way,
you don't have to worry about accidentally bumping the flaps up and down when operating a perpendicular axis on the same stick
(rudder for me). I put throttle and and flap gauges right in the central field of view so that you can see where they are set without
having to move the view around.

Just shortened the empennage slightly, which was spurred by finding it too long to spawn in a small-sized hangar. I think it looks better shorter anyway. To fit the small hangars, it was further necessary to then create a clip-wing variant without flaps. The roll control is quite poor, and even worse at high speed, but it makes a far better cruising machine than the Loach because the handling is way more stable than a helicopter, the cruise speed is much higher, plus the fuel is cheaper. Also, had to make the main landing gear super stubby, without shock absorbers, the retract for the nose wheel was removed, and it had to be mounted on a piston that extends when the plane spawns to raise the prop above the pavement. It only just barely fit.

# OH-6 Cayuse/Loach
I decided that the Cayuse would make an ideal game campaign vehicle due to its small size, low cost, versatility, and abiltiy to land anywhere.
This model came out pretty close-looking. Seating is for a pilot and nine passengers, five on the interior, and four perched outside by the skids and
door. Basically, I think this is going to be the smallest and most efficient VTOL rescue vehicle you could come up with, which does everything
except firefighting.

Takeoff is at about 4000rpm and 70% collective. Acceptable cruise can be accomplished at about 3000rpm, which adds some endurance. It has a fuel computer which tells you the fuel endurance, and if it's accurate, then you get like two hours from the dual fuel tanks. If you really have that much duration, I might remove a tank later, since the fuselage is just about packed full already. Endurance is down to 90mins after adding the weight of the
weapons. I don't know what else to add since this thing already has the kitchen sink. I wound up gearing the turbine way, way, down and the efficiency gains are huge, plus it spools up really slowly like the real thing.

I just added an anunciator panel for battery, fuel, RPM, and temp alarms.

Added position-hold and a rescue winch so that a single pilot can perform ocean rescues without landing, and without assistance. The winch has the annoying quirk that sometimes it won't fall off the ledge below the door, so let out some slack so that it's laying on the ledge, and then bump it with your feet to tip it over the lip. Then, get into it, and when you lower it further, you should go over and down. There are two harnesses and the brighter orange shade harness is the one that provides the controls to raise and lower the winch. I just added a remote control for the winch. That way, you can take the express elevator down (falling out of the helicopter), whether by accident, or intentionally, and you can still retrieve the harness remotely to get back up. Need to check to see if the radio remote will work from either harness, because it's a big help to not have to climb into a specific one. They tumble around a lot, and it sucks grabbing the specific one having controls in it. I just noticed you can bump the winch speed property way up, so that will help, too.

The position-hold is also a bit quirky. It seems to work most of the time, and especially if you are close to stationary when you engage it. When you turn it on, it stores the current 3D position and heading and attempts to maintain it. One strategy is to click it on, let it decelerate and stabilize you, and then click it off and on again, so that it doesn't try to laboriously drift back to where you first engaged it. It usually works, but I have seen it abruptly fail and let the helicopter drift off. I would love to figure out what causes that, since it seems improbable for it to work perfectly and then suddenly just give up holding the helicopter in place. It doesn't happen often enough that I've been able to pin it down. Also, keep in mind that it's a tiny helicopter which is CG-sensitive, so don't jostle it excessively moving around in it, or when placing passengers. I thought about leaving the rudder neutral on the theory that permitting the helicopter to weathervane minimizes the effort required of the cyclic, but unfortunately, what actually happens, is that it produces oscillation which results in circling and unpredictable drifting, so we lock the heading in place.

I initially had huge control problems which wound up boiling down to over-control and excessive power and collective, which are all easy to overdo given the power output of the turbine and the tiny size of the helicopter, weighing in at about a half ton. Once that was nailed down, it was easy to fix subtler problems, like CG issues, and the handling came out great. If you have problems with pitch control, your climb rate is probably excessive due to a high collective setting.

Added dual side-mounted light autocannons at 1000rds with HE and incendiary, and 32 rockets in underslung rocket pods. Also, a crosshair and ammo counters.
TODO: Includes making the hardpoints more modular and flexible, and adding a means to release unneeded weapon pods.

I did try a piston prototype using a medium standard engine, and it works really well. However, it totally messes up the CG and it would require a lot of work rearranging all of the innards. So, if I played and encountered a terrible jet fuel shortage, I might mess with that idea. I like the authenticity of the turbine, though, since that's how the real thing works.

# Prospector

I modified the Ranger for use as a mining rig after finding that the unloading sites are ground-level. Then I went to deliver my gold ore and found that you need a crane to deposit the dirt into the processing machine. So, this might be a dead end.

# Semi truck

The semi-truck is done and it works really well. It runs a bit hot despite an extensive cooling system, unfortunately. It could possibly be made more efficient by making the circuits parallel and not series, but I doubt it makes a huge difference. I made a slightly stretched mining truck version of the semi with a crane for loading the gold dirt hopper, and it also works great. I wound up developing the automatic transmission for the mining truck, and it needs backported to the base semi. The automatic transmission is pretty much a must-have because the engine torque is all over the place and it's a pain to manage manually. I will probably backport the mining truck back into the base semi-truck form, just deleting the mining stuff, and shortening it again.

# Fuel barge

Just a basic barge with a simple hull and a curved bow, holding 20 large-sized fluid tanks divided into two compartments, intended for making combind supply runs for both diesel and jet fuel. It has dolly wheels so that it can be spawned on land and towed into the water behind an amphibian like the APC in the collection.


# Hummelbird

Added a model of the Hummelbird. The real thing is about the smallest fully functional single-place fixed-wing piston prop GA aircraft to be found, and I'm really happy with this reproduction. As usual, it tends to come out a bit bigger because there is only so small that you can make the pilot's seat and cockpit. The performance and handling came out great, and the controls are very stable. Haven't figured out the range yet, but it's probably pretty good, since it's driven by a standard small engine fed with a single large fuel tank. Cruise is over 120knots, or somewhat more than the real thing. It seems to have the usual bad habits of an authentic tail-dragger on the ground. Beware of ground loops. It can be helpful to apply back-pressure on the stick in order to place pressure on the tail wheel, so that it will steer. There is a considerable nose-over tendency on the ground. There is no need for differential braking on such a tiny plane, when the tail wheel will turn it around on a dime. The up/down axis is used as a proportional brake applied to all of the wheels, in addition to the usual parking brake. The proportional brake should be applied very sparingly with plenty of back-stick to avoid nose-overs. Also, it's good to carry some throttle into the landing so that the drag on the wheels doesn't cause a nose-over either.

# Hummelfighter

The Hummelbird came out so well, I decided to take the somewhat improbable approach of making a fighter variant with twin wing-mounted light autocannons. It's not an entirely novel idea because there was an even smaller ultra-light class plane called the Vampire which was proposed as an extra-light weapons platform for military applications, but it seems as though the civilian design never went anywhere even though the specs were extremely impressive.

Anyway, the cannons are fed by 400rds in drums, and there is room for an additional pair of 200rd drums, but they impact the handling somewhat adversely, so they are left off by default, and are trivial to stick back on in the editor if you want to use the cannons for ground or water targets. The convergence on the guns is ground-adjustable through a property on an MCU in the nose. You can set the range at which the trajectories meet in front of the plane. If you set this too close, you will shoot your propeller off, Indiana Jones style. Historical WWII convergence ranges were somewhere around 350m.

I did attempt a gun interrupter so that the guns could be mounted converged on infinity on either side of the nose, firing through the propeller arc, but when you do the math at 2400 prop RPM, one game tick is more than 180 degrees of rotation, so there is no reliable way to time the guns.

# F16

This is a nimble single-engine jet fighter which was going to be modeled on the F16. However, I'm putting campaign functionality before cosmetic considerations, and there's just no in-game justification for the huge air scoop under the belly of the real thing, so this comes out a bit sleeker and simpler looking without that. I have read that you can sometimes wind up with far more efficiency and top speed by adding turbofan propulsion, because of quirks in how the jet thrust compares, so if I wind up adding that, then that might justify the addition of a big air scoop to house the fan.

Armament is twin nose-mounted light autocannons converged at infinity, and wing hard points which are populated with 48x in rocket pods by default. I ended up building this guy because I wanted a fast plane for strafing the AI armada early in the game, and missiles are just too expensive for that purpose. Small-scale AA missiles cost somewhere around $1600 apiece and are probably not enough take down a ship or boat, so by the time you were done sinking five ships, you would be out $16,000 in missiles, and there are simply better ways to invest that money early in the game.

The wheelbase on the landing gear is quite narrow, so turns on the ground should be completed at a low speed.
