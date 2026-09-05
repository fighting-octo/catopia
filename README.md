# 🐾 CATopia — Cat Café

A quiet cat café you can watch or join in with, built as a single self-contained HTML file.
Nothing in it demands attention: the bowls refill themselves, the cats feed themselves, and
nobody is ever unhappy with you. Every interaction is an offer, not a chore. The cats are drawn
with the same SVG artwork and animation style as the cats on fighting-octopus.com
(tail wave, head nod, blinking/sleeping eyes, four-leg walk cycle), extended into a
parametric coat generator so every cat looks different.

## Run it

Open `index.html` in a browser. No build, no dependencies, no server needed.
Progress is stored in `localStorage` and saves automatically.

## What's in it

**The café.** A room drawn in false perspective — angled side walls, a ceiling, and
floorboards that converge on a vanishing point. Framed cat paintings, a pinned MEOW poster
and pots of cat grass on the floor fill it out. Cats get smaller toward the back wall,
are depth-sorted so nobody is ever hidden behind another cat, and steer around each other
so they never walk through one another.

**The room next door.** Once the café is home to more than 15 cats it takes over the room
next door. The scene splits into two rooms side by side, each with its own back wall, window,
paintings, counter, diner, baskets, cat grass and cat trees — the second one decorated as a
quiet *nap room*. The wall between them has a doorway in it: a framed opening with a passage
floor running through, and the cats walk between the rooms as they please. They prefer the
bowls, beds and perches in whichever room they are in, and cross over when the room next door
has what they want (or just to see what's going on).

**The aquarium.** A big, lit fish tank is mounted on a wooden shelf along the café's left
wall, above head height, with brackets under the shelf and a soft shadow on the wall behind.
It runs almost the full length of the wall and stands about as tall as a cat, built as a box
in the room's own perspective — the front glass recedes toward the back corner, the water
surface runs along the top, and the near end cap shows the tank's thickness, so it reads as a
solid object rather than a flat panel. Thirteen little fish drift about inside at
their own speeds, changing their minds now and then, over gravel and swaying weed with a
stream of bubbles. They shrink as they swim toward the back of the tank, and are clipped to
the glass so none can slip out.

Because it hangs on the wall, the whole floor stays walkable — cats pass underneath it. Every
so often one wanders over, sits down below the glass and watches, which slowly makes it
happier (🐟 👀). A second cat picks a spot further along the tank rather than crowding the
first, and cats from the nap room come through the doorway to see it. Food or a toy breaks
the trance.

**The jellyfish mural.** A large jellyfish is painted along the café's right-hand wall, drawn
in the wall's own perspective so it recedes with it — a teal bell with pink oral arms and long
trailing tentacles that drift, plus two smaller ones and a scatter of bubbles. It's blended
into the wall rather than hung on it.

**Fountains and the litter tray.** Two little drinking fountains sit in opposite corners of
each room, water rippling in the bowl and a jet bubbling at the top. Cats stroll over for a
drink now and then. In the near-right corner there's a litter tray: a cat walks up beside it,
**hops in**, settles for about five seconds (with a bit of digging), then **hops out** and
carries on. Only one cat at a time, and the tray's near rim is drawn over them so they really
are inside it.

**Scratching and the armchair.** Every so often a cat wanders over to the scratching post or
the base of a cat tree, rears up on its hind legs and has a proper scratch — body tilted back,
front paws working alternately, tail swishing — then wanders off pleased with itself. Only one
cat per post at a time. In the near-right corner of each room there's a **comfy armchair** with
a buttoned back, rolled arms and a fat seat cushion; it counts as one of the room's beds, so cats climb
up and doze in it.

**On a phone.** The whole room scales to the screen — cats, furniture, bowls and the aquarium
all shrink together — the top bar compacts to short labels, the action bar scrolls sideways,
and the modals go full width with large tap targets. Tap a cat to open its card (and to bring
its 🥣 bowl button within reach); the laser pointer follows a finger.

**Naps.** A cat nap is a normal way to spend the afternoon here, not something that only
happens when a cat is exhausted. Calm cats nap most; busy ones keep pottering. At any moment
roughly a third of the café is asleep and the rest are up and about, and the sleepers are
spread around — baskets and cushions, the armchair, the cat trees, the shelves, the window
sill, the counter, and the warm lid of the fish tank.

**Climbing.** Each room has two cat trees — a short one and a tall one with a cushioned
platform on top — plus two wall shelves, a padded box bed on the top shelf, the window sill
and the counter. Cats walk to the base and jump up in a real arc, doze or sleep up there, and
jump back down when they want feeding or a toy appears.

**Visitors.** Every so often a butterfly drifts in through the café, or a mouse slips along by
the skirting board. Only the cats who happen to notice give chase — the playful ones, the
Hunters — while the rest carry on. Butterflies get hopeful leaps, mice get a scamper, and the
visitor eventually drifts up and out or vanishes into a corner. Cats that joined in come away
pleased with themselves. They arrive on their own, roughly once a café hour.

**Room to themselves.** Cats pick where to go by looking for the emptiest patch of floor
rather than a random one: a soft density field counts both where the other cats are and where
they're heading, and the quietest candidate wins, with a nudge toward actually going somewhere.
A cat won't sit down in the middle of a huddle — if its spot is crowded it keeps walking — and
one that finds itself hemmed in will get up and find its own corner. The bowls are spread the
width of the diner, and after eating a cat strolls off rather than loitering. In practice they
use about a quarter more of the room's width than they used to.

**Nobody crowds.** On top of the density scoring, every cat is given a loose patch of the room
of its own — the patches are spread evenly across the width and re-balanced as cats come and
go, so they drift back to different places rather than all to the same corner. A candidate spot
is also penalised sharply for being near *any single* cat, not just for overall busyness, which
is what stops pairs becoming trios. A cat won't sit down where it would make a third, it breaks
away from a huddle sooner the bigger the huddle is, it re-routes if its destination fills up on
the way, and it heads for the quietest free bowl rather than the nearest. In practice the
biggest group in the room drops from about 5 cats to 3–4, and the share of cats standing in a
group of three or more falls from ~15% to ~7%.

**Giving way.** When two walking cats meet head-on they don't shove past each other — the one
on the less urgent errand stops, steps aside, waits a beat, then carries straight on to where
it was going. Which cat yields is decided the same way every time, so they never dither. The
legs are also driven only by a cat's *own* walking, never by being nudged, so a jostle can no
longer start the walk cycle.

**Everyone on their own clock.** Every cat is born with a *restlessness* (shown on its card)
and a walking pace, nudged by its perks — a Lazy or Zen cat is a couch cat, a Speedy or
Mischievous one is a busybody. Restless cats set off across the room; calm ones mooch a few
steps and then sit down for anything from a few seconds to the best part of a minute. They
dawdle mid-walk at different rates, start the day out of step with each other, and pick up
speed at their own pace. In practice about half the café is on the move at any moment, and
which half keeps changing.

**Movement.** Cats always face the way they are going — the artwork is drawn facing left, so
a cat heading right is mirrored, and it turns around on the spot (a quick squash through the
turn) rather than ever walking backwards. Cats accelerate into a walk and ease to a stop rather than snapping between
speeds, drift along slightly curved paths instead of straight lines, and pause mid-stroll to
look at nothing. Their leg cycle is driven by the ground they actually cover — a cat that is
blocked or waiting stands still instead of walking on the spot — so nobody moonwalks. They
also look where they are going: a cat steers around anyone in its path, slows as it closes on
another cat, and stops to let them pass rather than walking into them. The animation itself is
damped so a jostle can't make it stutter: the walk/stand switch has hysteresis and a short
settling time, the step rate uses five fixed gears rather than being rewritten every frame, and
depth order is sticky, so two cats at the same depth can't swap in front of each other
frame by frame.
A cat never walks backwards: when it needs to go the other way it **turns around on the
spot** — a quick squash through the turn, then off in the new direction.

**Jumping** is a real arc: a crouch to gather, a stretch through the air with the legs tucked
and the tail streaming behind, and a squash on landing. Cats jump up to the sill, the
shelves, the tower and the counter — and back down again. They pounce on the ball and the
mouse toy from a short distance, spring straight up for the feather wand, and kittens,
acrobats and speedy cats skip along as they walk.

**Ten founding cats**, each with a different coat. They wander the floor, groom, chew the
cat grass, and settle
into the café's sleeping places: three wicker baskets and two floor cushions, plus high
spots they climb to — the window sill, both wall shelves, the padded box bed on the top
shelf, the two cat-tower platforms and (of course) the counter. Cats walk to a spot first,
then hop up; acrobats head straight for the high ones. They also lounge up there awake, and
come down when food or a toy appears. Everyone sleeps through the night (22:00–06:00),
and the window and room follow the café clock. From 19:00 the **indoor lights** come on — the hanging lamps brighten and cast warm pools over the floor, so the café stays cosy and easy to read all night while the window goes dark and the moon comes out.

**Cat cards & naming.** Every cat wears its name on a small tag in the room. Click any cat
to open its card: name, gender, age, coat/breed, perks, traits (appetite, playfulness,
agility, charm) and live condition bars (fullness, happiness, energy, bond). **Rename** it
from the card (the ✏️ Rename button or the pencil next to the name) — the tag in the room
updates immediately — and **click the ♀/♂ chip** to switch a cat's gender whenever you like.
Names carry a gender too: rename a cat *Oskar* or *Teddy* and it becomes a boy, *Luna* or
*Mochi* and it becomes a girl, and existing cafés are tidied up the same way once on load. From the card you can also pet it, play with it, treat it, or flag
where it is.

**Perks.** Every cat is generated with 1–3 of 18 perks that actually change behaviour —
`Lazy` cats keep their energy and ignore toys, `Acrobat` cats climb to high perches,
`Glutton` cats get hungry faster and eat bigger portions, `Picky Eater` cats nibble,
`Night Owl` cats stay up, `Sunbather` cats are happier by day, `Hunter` cats reach the toy
first, `Zen` cats stay content, `Charmer` cats cheer up their neighbours, and so on.

**The café feeds itself.** The bowls in the diner refill on their own a little while after
they're emptied, and the cats wander over and eat whenever they're hungry. You never have to
be there. The 🍽 button puts fresh food in every bowl if you feel like it, and treats are
always available — but nothing goes wrong if you just watch.

**Feeding one cat by hand.** Every cat has a small bowl button beside it — it glows and
pulses once that cat starts getting hungry, and appears on hover for the rest. Click it (or
🥣 Feed on the cat card) and pick from three foods:

| | | |
|---|---|---|
| 🥫 **Wet food** | +38 fullness, +8 happiness | a proper meal — counts as that cat's meal for the current window |
| 🍖 **Dry food** | +24 fullness, +3 happiness | a smaller top-up between meals |
| 🐟 **Treat** | +9 fullness, +16 happiness, +5 bond | barely food, but they love you for it |

The card also shows each cat's **restlessness**, which is why some of them are always up and
about while others barely leave their patch of floor.

The food is put out in a bowl in the **diner** — the mat beside the counter where all five
bowls live. That bowl fills up with the food you chose — pâté for wet, kibble for dry, pink
for treats — and lights up and bobs so you can see where the food went, the cat drops
whatever it was doing (it won't be distracted by toys on the way), walks over, lines itself
up beside the bowl and puts its head down into it to eat. This is the same for all three
foods — wet, dry and treats all go into a bowl in the diner. Each cat needs a little while before the next helping (the menu shows how
long). Hand-feed every cat wet food inside a meal window and you still get the perfect-
service 5 💗.

**Play.** Ball (physics + bounce), mouse toy, feather wand and a laser pointer that the
cats chase around the room with your cursor. The more cats join in, the more 💗 you earn.
Play also builds each cat's bond and burns energy.
Playing makes a real difference to a cat's mood: every pounce lifts its happiness, and when
the toy is put away each cat that joined in gets a further boost and a 😻. Cats never sink
below contented, so this is always a bonus rather than a rescue.

**💗 and kittens.** Affection collects slowly on its own while the café ticks along, and
faster when you join in — petting, playing, treats, and cats enjoying their food. At 12 💗 you
can introduce one ♀ and one ♂ grown cat in the breeding room. The kitten inherits coat
colours and patterns from both parents, one perk from each plus a chance of a fresh one,
averaged traits, and grows up after two café days. Max 24 cats, and no rush to get there.

**Time.** One real second = one café minute, so a full day is 24 minutes. ⏩ toggles 3×.
The clock keeps running in a background tab, and the cats drift (up to six café hours)
while the page is closed.
