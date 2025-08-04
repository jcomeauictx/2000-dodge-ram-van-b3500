2000 Dodge Ram Van B3500 Maintenance and Repair

August 2025, problem is like [this guy's](https://dodgeforum.com/forum/dodge-ram-van/443024-2000-ram-van-3500-crank-but-won-t-start.html). It was running fine
until the last trip, where on the way home the engine stalled when we had to
stop, but it started right back up both times. However, when we attempted to
start it a day or two after getting home, it doesn't start.

Some differences with Vincent's problems: first, bypassing the ASR[^1] relay by
jumpering pins 3 and 5 of the socket doesn't produce 12V at the DG/OR[^2] wire
of the ignition coil, and I can't see where the wire goes once it runs
behind the alternator. But I found out later, I must have jumpered it badly,
because grounding the other side of the coil pulled in the relay, and I had
my 12V at the ignition coil.

The code reader, Motopower MP60933, gets the display lit when connected to
the ODB2 receptacle under the steering wheel, but hitting the VIN or ODB key
attempts to communicate with the PCM[^1] and fails every time. I tested it with
a much newer Subaru Outback and it works, and the same model connects to
a Mercury Mountaineer from 2008 or so. So the code reader isn't likely at
fault. Turning the ignition key to "run" 3 times and waiting for the odometer
to flash results in the "no buS" display and the "check engine" light, followed
a minute or so later with the "low fuel" light.

Turns out it's totally unnecessary to do the on-off-on-off-on routine. It
flashes and shows "no buS" after just turning the key to "run", *once*,
and leaving it there for a minute.

I can't locate the fuel pump relay; it's neither in the engine bay fuse box
nor in the fuse panel behind the driver's door.

The wiring diagram in my Haynes manual shows a dark blue wire going from the
ignition run/start position to the ASR coil, but that's not the case. Instead
a red wire goes to the 30A fusible link marked 11 under the fuse box cover,
and a red wire with white stripe comes out the other side, splits into 2, and
connects to both the coil and common points on the relay. So it doesn't
require the ignition key at all to get voltage at the relay.

I found two of the spark plug connectors not seated properly at the distributor
cap, but that's unlikely to be relevant. Anyway, they're seated now.

If anything is wrong with the fuel system, I have no clue how to go about
fixing it, lacking the location of the relay, and not knowing for sure where
the fuel pump and filter are; however the best info I've found on YouTube
University indicates they're both in the fuel tank, which, full,
weighs on the order of 300 pounds.

I've removed the computer, cleaned the oxidation where it connects to the van,
and reconnected it; no help. Also cleaned and reconnected other ground wires.

Checked the TPS[^1], with the ignition key in RUN position,
for voltage, which should, according to one of the videos I watched but didn't
note the URL, indicate a (at least partly) function computer.
There were 5VDC at points 1 (OR --- Hayes manual shows VT/WT, and for pin 3,
as it has the pin numbers inverted) and 2 (OR/DB).  Pin 3 (BK/LB) showed no
voltage relative to ground.

2025-08-03: Earlier today, disconnected 3 sensors: CPS [^1],
located just under where the transmission dipstick tube goes into the floor
of the van; the connector is on the starboard side of the engine block.
Opposite that, on the port side, is the TPS. Disconnected
that too, and on the front of the engine block, whatever that sensor is.
Immediately after that, I turned the ignition key to "run" position and
plugged in the sensors in reverse order. After plugging in the one (camshaft
position sensor? Don't know) on the front of the engine block, I heard a
whirring behind the instrument cluster, the fuel gauge moved towards full,
and the "no buS" message was replaced by the odometer reading. Same happened
after reseating the TPS. Nothing happened, good or bad, while reconnecting
the CPS, so I started the van up, and it ran for a couple of minutes,
then died. Back to "no buS", no start.

Later, I disconnected and reconnected the upright sensor just to port of
the distributor, turned the key to "run", and saw the gauges working again,
so took the van downtown where someone else can look at it tomorrow.

Wiring diagram of PCM (computer), with C1 to the right as you're looking at it
from the front of the van:
![PCM connector C1](c1_e181c25b035a0ac079c3675bc15a4e60b2457ad4.gif)
![PCM connector C2](c2_7398725575682ba66f8fb8d72197ffdc16fc4d7b.webp)
![PCM connector C3](c3_1686aba26cfd12ff5fe27ea1fe5d29dbb9144111.webp)

[^1]: ASR: Automatic Shutdown Relay, PCM: Powertrain Control Module,
      AKA "the computer", TPS: Throttle Position Sensor,
      CPS: Crankshaft Position Sensor
[^2]: Color codes: DG=dark green; OR=orange; DB=dark blue; BK=black; YL=yellow;
      VT=violet; WT=white, GY=gray
