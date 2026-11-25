/* =====================================================================
   style.css — ONE shared stylesheet for all five pages of the Huwa site.
   WHAT IT IS:   the single source of styling for Home, About, Services,
                 Gallery and Contact.
   WHAT IT DOES: sets the color palette, fonts, header, hero, cards and
                 footer so every page looks like one site.
   WHAT IT MEANS: keeping all styling in one file means I change a color
                 once here and all five pages update together.
   ===================================================================== */

/* ---------------------------------------------------------------------
   1) GOOGLE FONTS
   WHAT IT IS:   an import of the two fonts chosen in the proposal.
   WHAT IT DOES: loads Playfair Display (headings) and Inter (body).
   WHAT IT MEANS: @import must be the very first rule or the browser
                 ignores it.
   --------------------------------------------------------------------- */
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700&family=Inter:wght@400;500;600&display=swap');

/* ---------------------------------------------------------------------
   2) DESIGN TOKENS (CSS VARIABLES)
   WHAT IT IS:   the brand palette and spacing, named once.
   WHAT IT DOES: stores the five proposal colors so every rule reuses them.
   WHAT IT MEANS: --primary in one place keeps the whole site consistent.
   --------------------------------------------------------------------- */
:root {
  --bg: #fdf8f3;        /* warm sand page background */
  --surface: #ffffff;   /* white cards */
  --primary: #7a3b2e;   /* deep Nubian red-brown: headings, buttons, links */
  --accent: #c46a3f;    /* warm orange: highlights and hover states */
  --text: #2b2b2b;      /* near-black body text (13.1:1 on --bg, passes AA) */
  --muted: #6b5d54;     /* softer brown for secondary text */
  --max: 1100px;        /* max content width so lines never get too wide */
  --radius: 14px;       /* shared rounded-corner size */
  --shadow: 0 10px 28px rgba(122, 59, 46, 0.12); /* soft brand-tinted shadow */
}

/* ---------------------------------------------------------------------
   3) RESET
   WHAT IT IS:   a tiny reset applied to every element.
   WHAT IT DOES: removes default margins and makes padding count inside width.
   WHAT IT MEANS: box-sizing: border-box stops padding from making boxes
                 wider than I expect.
   --------------------------------------------------------------------- */
* { margin: 0; padding: 0; box-sizing: border-box; }

/* ---------------------------------------------------------------------
   4) BASE / BODY
   WHAT IT IS:   the default look of the page and body text.
   WHAT IT DOES: sets background, text color, font and a comfortable
                 line-height; clamp() makes the body size fluid.
   WHAT IT MEANS: clamp(16px, 1.1vw, 18px) never drops below 16px on phones
                 and never grows past 18px on big screens.
   --------------------------------------------------------------------- */
body {
  background: var(--bg);
  color: var(--text);
  font-family: 'Inter', Arial, Helvetica, sans-serif;
  font-size: clamp(16px, 1.1vw, 18px);   /* FLUID body text (clamp #1) */
  line-height: 1.7;
}

/* Headings use the serif display font for a warm, cultural feel. */
h1, h2, h3 { font-family: 'Playfair Display', Georgia, serif; line-height: 1.15; color: var(--primary); }
h1 { font-size: clamp(32px, 6vw, 60px); }   /* FLUID h1 (clamp #2) */
h2 { font-size: clamp(24px, 3.4vw, 38px); } /* FLUID h2 (clamp #3) */
h3 { font-size: clamp(19px, 2vw, 23px); color: var(--text); }

/* Links default to the brand color. */
a { color: var(--primary); }

/* WHAT IT IS: global image rule. WHAT IT DOES: makes every image shrink to
   fit its container. WHAT IT MEANS: max-width:100% + height:auto stops any
   image from overflowing and causing horizontal scroll. */
img { max-width: 100%; height: auto; display: block; }

/* .container centers content and caps its width on large screens. */
.container { width: 100%; max-width: var(--max); margin: 0 auto; padding: 0 20px; }

/* ---------------------------------------------------------------------
   5) BUTTONS
   WHAT IT IS:   the shared call-to-action button style.
   WHAT IT DOES: draws a solid brand pill that darkens on hover.
   WHAT IT MEANS: one .btn class gives every CTA the same look.
   --------------------------------------------------------------------- */
.btn {
  display: inline-block;
  background: var(--primary);
  color: #fff;
  text-decoration: none;
  padding: 14px 30px;
  border-radius: 999px;      /* fully rounded pill */
  font-weight: 600;
  transition: background 0.2s ease, transform 0.2s ease;
}
.btn:hover { background: var(--accent); transform: translateY(-2px); } /* lift + warm up on hover */
.btn--ghost { background: transparent; color: var(--primary); border: 2px solid var(--primary); }
.btn--ghost:hover { background: var(--primary); color: #fff; }

/* ---------------------------------------------------------------------
   6) STICKY HEADER (reused on every page)
   WHAT IT IS:   the top bar with the logo on the left and nav on the right.
   WHAT IT DOES: display:flex puts them on one row; justify-content:
                 space-between pushes them to opposite ends; position:sticky
                 keeps the bar pinned while scrolling.
   WHAT IT MEANS: space-between = logo far left, nav far right, gap in middle.
   --------------------------------------------------------------------- */
.site-header {
  position: sticky;
  top: 0;
  z-index: 50;                         /* stays above page content */
  background: var(--surface);
  box-shadow: 0 2px 10px rgba(0,0,0,0.06);
}
.site-header .container {
  display: flex;
  justify-content: space-between;      /* logo left, nav right */
  align-items: center;                 /* vertically centered */
  min-height: 70px;
}

/* Logo lockup: the inline SVG mark plus the site name. */
.logo { display: flex; align-items: center; gap: 10px; text-decoration: none; }
.logo__name { font-family: 'Playfair Display', serif; font-size: 22px; font-weight: 700; color: var(--primary); }

/* Nav links sit in a row with even spacing. */
.nav__list { list-style: none; display: flex; gap: 26px; }
.nav__list a { text-decoration: none; color: var(--text); font-weight: 500; padding: 6px 2px; }
.nav__list a:hover { color: var(--accent); }

/* WHAT IT IS: the hamburger button. WHAT IT DOES: hidden on desktop, shown
   on small screens. WHAT IT MEANS: display:none now; the mobile media query
   turns it on so the nav can collapse behind it. */
.nav-toggle {
  display: none;
  background: none;
  border: 0;
  font-size: 26px;
  color: var(--primary);
  cursor: pointer;
}

/* ---------------------------------------------------------------------
   7) HERO (Home page)
   WHAT IT IS:   the full-height first impression under the header.
   WHAT IT DOES: a warm gradient panel that fills the screen and centers
                 its text with a Flexbox column.
   WHAT IT MEANS: min-height:80vh = at least 80% of the screen tall, so it
                 feels intentional; the flex column-center trio stacks and
                 centers the h1, subhead and button.
   --------------------------------------------------------------------- */
.hero {
  min-height: 80vh;                    /* fills most of the screen */
  display: flex;
  flex-direction: column;              /* stack items vertically */
  justify-content: center;             /* center them up-and-down */
  align-items: center;                 /* center them left-and-right */
  text-align: center;
  gap: 18px;
  padding: 60px 20px;
  background: linear-gradient(160deg, #fdf8f3 0%, #f3ddc9 60%, #e9c6a6 100%);
}
.hero p { max-width: 620px; color: var(--muted); font-size: clamp(16px, 1.6vw, 20px); }
.hero__actions { display: flex; flex-wrap: wrap; gap: 14px; justify-content: center; margin-top: 8px; }

/* ---------------------------------------------------------------------
   8) GENERIC SECTION SPACING
   --------------------------------------------------------------------- */
.section { padding: 70px 0; }
.section__head { text-align: center; max-width: 640px; margin: 0 auto 40px; }
.section__head p { color: var(--muted); margin-top: 10px; }

/* Full-width image band showing Nubian life. */
.glimpse { margin: 0 auto; max-width: var(--max); padding: 0 20px; }
.glimpse img { width: 100%; border-radius: var(--radius); box-shadow: var(--shadow); }
.glimpse figcaption { text-align: center; color: var(--muted); font-size: 15px; margin-top: 12px; }

/* ---------------------------------------------------------------------
   9) FEATURE CARDS
   WHAT IT IS:   the three-card row.
   WHAT IT DOES: flex with flex-wrap lets the cards sit side by side on wide
                 screens and wrap to a stack on narrow ones.
   WHAT IT MEANS: flex:1 1 280px = each card grows/shrinks but never gets
                 narrower than 280px, so it drops to the next line instead
                 of overflowing.
   --------------------------------------------------------------------- */
.cards { display: flex; flex-wrap: wrap; gap: 26px; justify-content: center; }
.card {
  flex: 1 1 280px;
  max-width: 340px;
  background: var(--surface);
  border: 1px solid #eadfd5;
  border-radius: var(--radius);
  padding: 30px 26px;
  box-shadow: var(--shadow);
  transition: transform 0.2s ease;
}
.card:hover { transform: translateY(-6px); }  /* gentle lift on hover */
.card__icon { font-size: 38px; }              /* emoji icon */
.card h3 { margin: 14px 0 8px; }
.card p { color: var(--muted); }

/* ---------------------------------------------------------------------
   10) REPEAT CTA band
   WHAT IT IS:   the second call-to-action lower on the page.
   WHAT IT DOES: a solid brand band with centered text and a button.
   WHAT IT MEANS: repeating the CTA gives a scrolling visitor a second,
                 obvious way to reach the Contact page.
   --------------------------------------------------------------------- */
.cta {
  background: var(--primary);
  color: #fff;
  text-align: center;
  padding: 64px 20px;
}
.cta h2 { color: #fff; }
.cta p { color: #f3d9cc; max-width: 560px; margin: 12px auto 24px; }
.cta .btn { background: #fff; color: var(--primary); }
.cta .btn:hover { background: var(--accent); color: #fff; }

/* ---------------------------------------------------------------------
   11) FOOTER (reused on every page)
   --------------------------------------------------------------------- */
.site-footer { background: #2b1b15; color: #f3e7de; padding: 40px 0; }
.site-footer .container { display: flex; flex-wrap: wrap; justify-content: space-between; gap: 18px; }
.site-footer a { color: #f3c9ad; text-decoration: none; }
.site-footer a:hover { text-decoration: underline; }
.site-footer__social { display: flex; gap: 16px; }

/* Simple styling for the placeholder stub pages. */
.stub { min-height: 60vh; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; gap: 14px; padding: 60px 20px; }
.stub p { color: var(--muted); max-width: 520px; }

/* ---------------------------------------------------------------------
   12) MOBILE BREAKPOINT (below 768px)
   WHAT IT IS:   the small-screen adjustments.
   WHAT IT DOES: shows the hamburger, hides the nav until JS opens it, and
                 stacks the footer.
   WHAT IT MEANS: on phones the full nav would not fit, so it collapses
                 behind the ☰ button; script.js toggles .nav--open.
   --------------------------------------------------------------------- */
@media (max-width: 767px) {
  .nav-toggle { display: block; }       /* show the hamburger */

  .nav {
    position: absolute;
    top: 70px; left: 0; right: 0;
    background: var(--surface);
    box-shadow: 0 8px 16px rgba(0,0,0,0.1);
    display: none;                       /* hidden until opened */
  }
  .nav.nav--open { display: block; }     /* JS adds this class on tap */
  .nav__list { flex-direction: column; gap: 0; padding: 10px 20px; }
  .nav__list a { display: block; padding: 12px 0; border-top: 1px solid #efe3d8; }

  .site-footer .container { flex-direction: column; text-align: center; }
  .site-footer__social { justify-content: center; }
}

/* =====================================================================
   13) ABOUT PAGE
   Styles used only on about.html: the short page hero, the two-column
   "Our Story" grid, the auto-fit "What We Believe" grid, and the callout.
   ===================================================================== */

/* Short page hero (not full-height like the Home hero). */
.page-hero {
  background: linear-gradient(160deg, #fdf8f3 0%, #f3ddc9 100%);
  padding: 56px 0 44px;
  text-align: center;
}
.page-hero p { color: var(--muted); margin-top: 8px; }

/* A tinted section background to separate "What We Believe". */
.section--tint { background: #f7ede3; }

/* WHAT IT IS: the Our Story layout. WHAT IT DOES: two equal columns side by
   side on desktop. WHAT IT MEANS: grid-template-columns: 1fr 1fr = two equal
   tracks; gap adds space between them. */
.story {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 32px;
  align-items: center;
}
.story__text h2 { margin-bottom: 12px; }
.story__text p { color: var(--muted); margin-bottom: 14px; }
.story__media img { border-radius: var(--radius); box-shadow: var(--shadow); width: 100%; }

/* WHAT IT IS: the values grid. WHAT IT DOES: lays the cards in as many columns
   as fit. WHAT IT MEANS: repeat(auto-fit, minmax(240px, 1fr)) makes each
   column at least 240px and shares the leftover space — responsive with no
   media query. */
.values {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 24px;
}
.value {
  background: var(--surface);
  border: 1px solid #eadfd5;
  border-radius: var(--radius);
  padding: 28px 24px;
  box-shadow: var(--shadow);
  text-align: center;
}
.value__icon { width: 46px; height: 46px; margin: 0 auto 10px; display: block; }
.value h3 { margin-bottom: 8px; }
.value p { color: var(--muted); }

/* WHAT IT IS: the pull-quote callout. WHAT IT DOES: a tinted block with a thick
   colored left border so it stands apart. WHAT IT MEANS: border-left is the
   accent stripe that signals "this is a highlighted quote". */
.callout {
  background: #fbf1e8;
  border-left: 6px solid var(--accent);
  border-radius: 8px;
  padding: 24px 28px;
  max-width: 760px;
  margin: 0 auto;
}
.callout p { font-family: 'Playfair Display', Georgia, serif; font-size: clamp(18px, 2.4vw, 24px); color: var(--primary); font-style: italic; }

/* Stack the Our Story columns on phones (below 600px). */
@media (max-width: 600px) {
  .story { grid-template-columns: 1fr; }   /* one column, image under text */
}

/* =====================================================================
   14) SERVICES PAGE (services.html) — our own CSS, not Tailwind.
   The services grid uses the auto-fit recipe so cards reflow on their own.
   ===================================================================== */

/* WHAT IT IS: the services grid. WHAT IT DOES: lays the cards in as many
   columns as fit (1 on phones, up to 4 on wide screens). WHAT IT MEANS:
   repeat(auto-fit, minmax(240px, 1fr)) means "make each column at least 240px
   and share the leftover space" — responsive with no media query. */
.services {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 24px;
}

/* WHAT IT IS: one service card. WHAT IT DOES: a white card holding an icon,
   title, description and a call-to-action. WHAT IT MEANS: flex-direction
   column stacks the parts and margin-top:auto on the button pins it to the
   bottom so every card's button lines up. */
.service {
  background: var(--surface);
  border: 1px solid #eadfd5;
  border-radius: var(--radius);
  padding: 28px 24px;
  box-shadow: var(--shadow);
  display: flex;
  flex-direction: column;
  /* WHAT IT DOES: animates the lift on hover. WHAT IT MEANS: transition makes
     the transform and shadow change smoothly instead of snapping. */
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

/* Hover effect: a subtle lift plus a larger shadow. */
.service:hover {
  transform: translateY(-4px);
  box-shadow: 0 16px 34px rgba(122, 59, 46, 0.18);
}

.service__icon { width: 48px; height: 48px; margin-bottom: 12px; }
.service h3 { margin-bottom: 8px; }
.service p { color: var(--muted); margin-bottom: 18px; }

/* Small button variant, and push it to the bottom of the card. */
.btn--sm { align-self: flex-start; margin-top: auto; padding: 9px 20px; font-size: 15px; }

/* =====================================================================
   15) GALLERY PAGE (gallery.html)
   Photo grid (auto-fit) plus the video/audio media blocks.
   ===================================================================== */

/* WHAT IT IS: the photo grid. WHAT IT DOES: fits as many ~240px columns as
   the screen allows. WHAT IT MEANS: repeat(auto-fit, minmax(240px, 1fr)) is
   responsive with no media query. */
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 18px;
}

/* WHAT IT IS: one photo cell. WHAT IT DOES: holds the image and its caption.
   WHAT IT MEANS: margin:0 removes the browser's default <figure> margin. */
.photo { margin: 0; background: var(--surface); border-radius: var(--radius); overflow: hidden; box-shadow: var(--shadow); }

/* WHAT IT DOES: forces every photo to the same size and crops it.
   WHAT IT MEANS: object-fit: cover fills the box without stretching the
   picture, so tall and wide photos all look tidy. */
.photo img { width: 100%; height: 200px; object-fit: cover; display: block; }
.photo figcaption { padding: 10px 14px; font-size: 14px; color: var(--muted); }

/* WHAT IT IS: the video + audio layout. WHAT IT DOES: two columns on wide
   screens, stacked on phones. */
.media { display: grid; grid-template-columns: 1fr 1fr; gap: 24px; }
.media__item { margin: 0; background: var(--surface); border: 1px solid #eadfd5; border-radius: var(--radius); padding: 16px; box-shadow: var(--shadow); }

/* WHAT IT DOES: keeps media inside its box. WHAT IT MEANS: max-width:100%
   stops the video or audio bar from overflowing the screen on phones. */
.media__item video, .media__item audio { width: 100%; max-width: 100%; display: block; border-radius: 8px; }
.media__item figcaption { margin-top: 10px; font-size: 14px; color: var(--muted); }

/* Stack the two media items on phones. */
@media (max-width: 600px) {
  .media { grid-template-columns: 1fr; }
}

/* =====================================================================
   16) CONTACT PAGE (contact.html)
   Two columns: the form on the left, contact details on the right.
   ===================================================================== */

/* WHAT IT IS: the contact layout. WHAT IT DOES: form and details side by side
   on desktop. WHAT IT MEANS: 1.4fr 1fr gives the form a bit more room. */
.contact-grid {
  display: grid;
  grid-template-columns: 1.4fr 1fr;
  gap: 40px;
  align-items: start;
}

/* The form card. */
.contact-form {
  background: var(--surface);
  border: 1px solid #eadfd5;
  border-radius: var(--radius);
  padding: 28px;
  box-shadow: var(--shadow);
}

/* WHAT IT IS: one form field. WHAT IT DOES: stacks the label above its input.
   WHAT IT MEANS: display:block on the label puts it on its own line. */
.field { margin-bottom: 18px; }
.field label { display: block; font-weight: 600; margin-bottom: 6px; color: var(--text); }
.field .opt { font-weight: 400; color: var(--muted); font-size: 14px; }

/* Inputs and textarea share one look; box-sizing keeps them inside the card. */
.contact-form input,
.contact-form textarea {
  width: 100%;
  box-sizing: border-box;
  padding: 12px 14px;
  border: 1px solid #d8c9bb;
  border-radius: 8px;
  font-family: inherit;
  font-size: 16px;
  background: #fffdfb;
  color: var(--text);
}
.contact-form textarea { resize: vertical; }

/* WHAT IT DOES: a clear focus ring. WHAT IT MEANS: focus-visible shows keyboard
   users exactly which field they are in, which the browser needs for a11y. */
.contact-form input:focus-visible,
.contact-form textarea:focus-visible {
  outline: 2px solid var(--primary);
  outline-offset: 1px;
  border-color: var(--primary);
}
.contact-form .btn { border: 0; cursor: pointer; margin-top: 6px; }

/* Contact details panel on the right. */
.contact-details { background: #fbf1e8; border-radius: var(--radius); padding: 26px; }
.contact-details h2 { font-size: clamp(20px, 2.4vw, 26px); margin-bottom: 14px; }
.contact-details p, .contact-details address { margin-bottom: 16px; color: var(--text); font-style: normal; line-height: 1.6; }
.contact-details a { color: var(--primary); }

/* Stack the two columns on phones. */
@media (max-width: 700px) {
  .contact-grid { grid-template-columns: 1fr; }
}
