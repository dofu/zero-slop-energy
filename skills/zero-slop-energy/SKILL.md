---
name: zero-slop-energy
description: Check design and writing for the habits that make work look AI-generated and say what to use instead. Use this skill whenever the user asks whether something looks like AI slop, generic, templated or vibecoded, or asks to check for AI tells, in a Figma frame, web page, dashboard, slide, carousel or piece of copy. Also read it BEFORE designing or writing anything visual, so each default is chosen on purpose and not by accident. Fixes findings only when asked. It is not a general design review and does not judge usability, accessibility or brand fit.
---

# Zero slop energy

"AI slop" is the set of visual and written habits that make work look generated: defaults nobody chose, decoration with no job, claims with no source. This skill checks a piece of work against a list of those tells and says what to use in place of each one.

It works on Figma files and equally on web pages, slides, carousels, articles and UI copy.

## How to run a check

1. **Know what is being checked.** A Figma frame or selection, a file, or pasted text. If it is not clear which, ask once.
2. **Report first.** List what was found. Change the work only when asked to fix it and then change only the things named. In Figma, someone may be editing the same frame, so read its current state before any edit and never rebuild or remove a frame to fix one detail.
3. **Look at the picture as well as the data.** Layer properties find a gradient or a one-sided stroke; only a render shows whether a screen as a whole reads as generated. Check both.
4. **One line per finding:** the tell, where it is (layer name and a link to the node, or file and line) and what to use in its place. No findings: say so in one line. From a screenshot there are no layers to name: describe the place in words ("the orange line above the title") and say what a still picture cannot show, such as layer names, motion or the exact colour of a thin outline.
5. **Ask what is deliberate before counting.** After the list, ask once which findings are on purpose or come from the design system or the brand guide and leave those out of the count. If the designer is not sure, or the screen was generated, say which one or two findings matter most here. Purple is fine when purple is the brand colour; the tell is the default purple gradient on everything.

### Reading a Figma file

- Take the frame's structure once and work from it: text layers give all the copy, fills and strokes give colours and borders, instance names give icons and the page, frame and layer names are checked too (C9). This costs far fewer calls than a screenshot per element and some Figma plans cap calls per hour.
- Then render only the frames whose overall look matters.
- Give every finding a link to the most specific node that can be linked. A layer inside a component instance cannot be linked; link its nearest frame.

## Fixing

Fix only when asked and only the findings named.

1. **Gather first.** The file's own variables, styles and components; the real content; what the screen is for and its one main action. If any of these is missing, ask. Do not invent a brand colour, a number or a name.
2. **Fix in this order:** content, hierarchy, colour and type from the file's own tokens, then remove decoration.
3. **In Figma:** bind to existing variables and styles, use existing components, change the smallest thing that fixes the finding and keep every frame in place.
4. **Check.** Render again, count again and list what remains and why.

## Before designing

Read the lists first to know the defaults and choose each one on purpose. The brand guide and the design system come first. Gather the three things in step 1 of Fixing before drawing anything.

## Count them, do not ban them

One or two of these on a screen mean little. Most are defaults and some are good choices in the right place. What reads as generated is many of them at once.

As a rule of thumb, per screen:

- 0 to 3: reads as chosen.
- 4 to 6: reads as mostly defaults, with some choices.
- 7 or more: reads as all defaults.

The bands describe how the screen reads, not how it was made. For a single card or component, list the findings and give no band. Give the count after the designer has said which findings are deliberate.

Removing one default look does not make work original. Asked for "less AI", a model moves to the next most likely look: from purple gradients, glows and glass (V1, V2, V17, V18, V25), to cream paper and editorial serif (V9, V13), to near-black with an acid accent (V20). The way out is the same each time: real design tokens, type chosen for the subject and real content leading the layout.

In the tables below, the last column is a suggestion. The brand guide and the design system come first.

## Visual tells

| | Tell | How to spot it in Figma | Use in its place |
|---|---|---|---|
| V1 | **Purple or violet gradient on everything**: backgrounds, buttons, headline text | Gradient fills whose stops sit in the blue-violet to magenta range, on several unrelated layers; gradient fills on text | One brand colour, kept for actions. Flat fills. |
| V2 | **Round glow in the background**: large soft circles or blobs of colour behind the content | Ellipses with a large layer blur, or radial gradient fills that fade to transparent, sitting behind everything else; layers named Glow, Blur, Blob or Ellipse | A flat background, or an image with a reason to be there. |
| V3 | **Hero badge**: a pill above the headline reading NEW, AI-POWERED, BETA | A small rounded frame with uppercase text, directly above the largest text on the screen | Say what the product is in the headline. Drop the pill. |
| V4 | **Fake proof**: "Trusted by 10,000+ teams", a row of grey logos nobody supplied | Text matching "trusted by", "loved by", "join N+"; a row of placeholder logo shapes | Name real users, or leave the line out. |
| V5 | **Sparkle icon on buttons and labels** | Icon instances named sparkle, sparkles, stars, magic, wand or ai, inside buttons | Label the action ("Summarise notes"), not the technology. One accent per screen at most. |
| V6 | **Fake terminal or code window as the hero** on a product for people who do not code | A dark frame with three small circles in a row and monospaced text | The real screen people will use. |
| V7 | **Decorative numbers and filler cards**: giant faded numerals, dot grids, stat tiles with nothing behind them | Very large text at low opacity; cards that hold only an icon and a noun | Remove. Every element gives the user something to read or do. |
| V8 | **Thick one-sided accent bar** on a card, note, quote or callout | Per-side stroke weights where one side is 2 px or more and the rest are 0; a thin rectangle flush to one edge of a card; an inset shadow with an offset and no blur | A tint, a full outline, a dashed outline, or nothing. |
| V9 | **The editorial house look**: a centred serif headline with one italic word in the accent colour, usually a feeling word (effortless, human, calm) and a full stop; numbered labels ("01 / Problem"); uppercase monospaced labels with wide letter spacing | Italic serif on the largest text with one differently coloured character; text matching a number, a slash and a word; monospaced uppercase text with letter spacing above about 5% | Section labels as quiet sentence-case text. Monospace only for numbers and code. |
| V10 | **Pixel or novelty fonts for text people read or count** | Text layers in a pixel font holding sentences, numbers or codes (C reads as O, 5 as S) | Pixel art for icons only. A rounded or plain body face for anything read. |
| V11 | **Display type far outside the page's own scale** | Text sizes with no matching text style, much larger than the largest style | Use the type scale. If there is none, make one and stay inside it. |
| V12 | **Placeholder content**: lorem ipsum, "John Doe", round numbers, three-letter names | Text matching lorem, ipsum, John Doe, Jane Doe; every amount ending in 00 | The longest and most awkward real values. A layout tested on short fake content proves nothing. |
| V13 | **Cream paper and one rust accent**: an off-white page, no pure white or black, one terracotta or clay colour on buttons and marks (the same move in sage or forest green is the same tell) | Page fill a warm off-white; text a warm near-black; exactly one saturated colour in the file | Colours from your own design system or brand, chosen for a reason you can state. |
| V14 | **Three equal feature cards**: a line icon in a tinted rounded square, a two-word title, one line of text ("Lightning fast", "Secure by default", "Built for teams") | Three sibling frames of the same size in a row, each with a small square icon holder, a title and a short text | Show the one thing the product does, with the real screen. Unequal content gets unequal space. |
| V15 | **Pill button beside a ghost arrow link** ("Get started", "See how it works" with an arrow) | A fully rounded filled button followed by a text link ending in an arrow | One primary action. A second one only if people need it, named for what it does. |
| V16 | **Hairlines and soft corners on everything**: 1 px warm borders, 12 to 16 px radii, a faint shadow, all at once on every container | Most frames share the same 1 px stroke, the same radius and the same light drop shadow | Borders, radii and shadows that mean something: a border where things separate, a shadow where something floats. |
| V17 | **Glass cards**: translucent panels with a background blur, often over a glow | Frames with a background blur effect and a low-opacity white or dark fill | Solid surfaces. Blur only where content really sits over moving or photographic content. |
| V18 | **Emoji used as icons** | Text layers holding a single emoji inside buttons, cards or list rows | The product's own icon set, or no icon. |
| V19 | **Asterisk or burst logo** standing in for a brand mark | A star, asterisk or sunburst shape beside the product name in the header | The real logo, or the name set in plain type. |
| V20 | **Acid noir**: near-black page, one acid green or vermilion accent, monospaced type throughout, a visible grid | Near-black page fill, a grid of thin lines as background, monospaced fonts on headings and body | Same as V13: a palette and type chosen for the subject, not the next default in line. |
| V21 | **One colour on everything**: headings, links, icons, borders, tags and buttons all in the same accent, so nothing stands out | The same fill style or colour variable on heading text, icons, strokes and button fills; a large share of the layers on a screen carrying the accent | Keep the accent for the action. Headings and text in the neutral ink; hierarchy from size, weight and space. |
| V22 | **One default font on everything**: the tool's stock sans (Inter most often; also Roboto, Open Sans, the system font) on every heading, button and paragraph, with no choice behind it | One font family across every text layer and it is the design tool's or framework's default | A face picked for the subject, or the product's own. Real contrast between heading and body in size and weight. |
| V23 | **An icon on every point**: each bullet, heading or card gets its own icon, so every point carries the same weight and none of the icons says anything | An icon instance beside every list row or above every heading in a section; a different icon for each, all the same size | Icons only where they help someone find or recognise a thing. Group related points and let the important one be bigger. |
| V24 | **Stock entrance motion**: every section fades in from below as it scrolls into view, same distance, same timing, staggered | In a prototype, the same move-in on every frame; in code, opacity with a vertical shift of about 600 ms and a 100 ms stagger on everything | Motion only where it explains a change. Most content needs none. |
| V25 | **Glow around buttons**: a soft coloured halo behind the main button, often on cards and inputs too | A drop shadow with no offset, a large blur and the button's own colour instead of a neutral one; the same effect repeated on several components | A flat fill. A neutral shadow only where something floats above the page. A clear outline for keyboard focus, which is a different job. |

## Product UI tells

The visual list above leans towards landing pages. These show up inside the product: cards, lists, detail screens, dashboards. From the visual list, V12, V16, V21, V23 and V25 are the ones seen most often in product screens as well.

U1 and U3 depend on what one card or a screenshot cannot show: whether the lines repeat on every card and whether the card is in a state such as selected. With only one card or a still picture, ask that first and list them only if the answer makes them a finding.

| | Tell | How to spot it in Figma | Use in its place |
|---|---|---|---|
| U1 | **A hairline under every row**: label on the left, value on the right, a thin line after each, on every card | Rows of two text layers with a 1 px line or bottom stroke between all of them; the same row repeated down the card | Space to separate rows that are alike. A line only between groups that differ. Let the one value people came for be larger than the rest. |
| U2 | **An uppercase accent line that chains claims with middle dots** above the title ("START HERE · FROM 1,000 · MOST BOUGHT") | A small uppercase text layer in the accent colour, above the card title, holding two or more middle dots | One short label, or none. Put each fact where it belongs on the card. |
| U3 | **A dark card with a thin accent-colour outline** | A dark fill with a 1 px stroke in the accent colour, on cards that are not selected or focused | Keep the outline for a state: selected, focused, in error. Separate resting cards by surface colour or space. |
| U4 | **Small grey labels over large coloured figures**, with no date or basis | Pairs of a small muted text layer above a large coloured number, in a row at the foot of a card; no "as of" text near them | Say what the figure measures and as of when. Colour only where it carries meaning that is also given in words or a sign. |

## Dashboard tells

| | Tell | How to spot it in Figma | Use in its place |
|---|---|---|---|
| D1 | **Four equal metric cards in a row** at the top of the screen: an even strip of highlights with none of them emphasised | Four sibling frames of the same size, each a label and a large number | One figure leads, larger than the rest. The others sit smaller beside or under it. |
| D2 | **Every panel the same size**, so the figure that matters sits in the same box as a minor one | All cards on the screen share one width and one height | Size by importance. Dense detail goes in one divided card, not a stack of equal ones. |
| D3 | **Figures nobody acts on**: totals such as revenue, users or sessions, with nothing late, due or waiting | Metric labels that are all totals; no figure tied to a date, a limit or a person | Figures that change what someone does next ("12 invoices overdue"). |

## Figma file tells

These are about how the file is built, not how the screen looks. A screen can look finished and still be unusable as a design file.

| | Tell | How to spot it in Figma | Use in its place |
|---|---|---|---|
| F1 | **A flat image where layers should be**: a screen, card, chart or illustration that is one picture, so nothing in it can be selected, edited, resized or inspected | A frame whose only content is a rectangle with an image fill; words on the screen but no text layers; an image fill that itself shows buttons and text | Real layers: text as text, shapes as vectors, layout as auto layout, repeated parts as components. An image only for what is truly a picture. |

## Copy tells

| | Tell | Use in its place |
|---|---|---|
| C1 | **"It's not X. It's Y."** taglines and "second brain", "superpower" copy | One plain sentence saying what it does for the person. |
| C2 | **Made-up stats**: 10x faster, 99.9% uptime, 120+ integrations | A number that was measured or has a source, with its unit and its basis. Otherwise no number. |
| C3 | **Filler copy**: a caption, subline or helper text that repeats what the layout already says, or says nothing ("Built for teams who care about craft") | Ask what the reader can do differently after reading it. If nothing, cut it. Prefer one specific fact: a minimum, a date, a limit. |
| C4 | **Em dashes, en dashes and arrow symbols** in running text | Commas, full stops, semicolons or brackets. |
| C5 | **Stock AI vocabulary**: delve, testament, tapestry, beacon, realm, elevate, revolutionize, undoubtedly, moreover, furthermore, "in conclusion", "it is important to note" | The plain word, or delete the sentence. |
| C6 | **Patterned sentences**: "not only... but also", stacked adjectives ("a vibrant, bustling city"), every bullet the same length and shape, a closing paragraph that repeats the text above | Vary sentence length. Uneven bullets. End when the content ends. |
| C7 | **Customer-service tone**: cheerful openers, robotic politeness | Direct and conversational. |
| C8 | **Invisible characters**: zero-width spaces and similar, left behind by generated text | Strip them. |
| C9 | **Em dashes and middle dots in names**: file names and Figma page, frame and layer names such as "Checkout — Final" or "Card · Hover" | Plain words. A slash for hierarchy in Figma ("Card / Hover"), a hyphen in file names ("checkout-final"). |

## Checking work that is not in Figma

- **Code and text files:** search for the characters and words in C4, C5 and C8 and list file names for C9; for `border-left`, `border-right`, `border-top` and inset `box-shadow` stripes (V8); for gradient declarations (V1); for large blurred or radial-gradient circles behind the content (V2).
- **Slides and carousels:** render every slide and check each against the visual, product UI and dashboard lists; read every line against the copy list.

## Better options

When a tell is removed, something better can often take its place:

- a real screenshot with pointers, in place of a mock
- a measured before and after pair
- a timeline built from real timestamps
- a plain table of values with their source
- a real quote with the person's role, or no quote

