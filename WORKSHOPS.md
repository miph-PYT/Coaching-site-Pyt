# How to add a workshop

You add and edit workshops in **Pages CMS**, a simple editor for this website. You don't need to touch any code. Every time you save, Pages CMS updates the website, and the change is live after 1–2 minutes.

---

## 1. Open the editor

1. Go to **https://app.pagescms.org** and click **Sign in with GitHub**. Use the GitHub account that owns this repository (`miph-PYT`).
2. Choose the repository **Coaching-site-Pyt**, branch **main**.
3. In the left menu you'll see **Blog posts** and **Workshops**. Click **Workshops**.

## 2. Add a new workshop

1. Click **Add an entry**. A new, empty workshop appears at the bottom of the list.
2. Fill in the fields (see the table below). Only **Title** and **Web address** are required.
3. Click **Save**.

That's it. Give the website 1–2 minutes, then refresh **www.parts-work.dk/workshops.html**. Your new workshop appears under **More workshops**, and it has its own page.

## 3. What each field does

| Field | What to write | Example |
|---|---|---|
| **Title** | The name of the workshop. | Coffee with Your People-Pleaser |
| **Web address** | A short name for the link: lowercase, dashes instead of spaces, no special letters (æ, ø, å). Must be different for every workshop. | `people-pleaser` |
| **Status** | Pick one: *Open for sign-up*, *On request* or *Coming soon*. Shown as a small label. | On request |
| **One-line description** | One sentence under the title. | Saying no without the guilt. |
| **Length** | How long it takes. | 2 hours |
| **Language** | Which language(s). | English or Danish |
| **Group size** | Leave empty to hide it. | 6–14 people |
| **Price** | Leave empty to hide it. | 250 kr |
| **Next date and venue** | Leave empty and the page says *"Dates announced soon"* with an **Ask about dates** button. Fill it in and the button changes to **Save me a seat**. | Thursday 15 January, 17:00, Café X |
| **What to bring** | | A notebook and a pen |
| **Intro text** | A few paragraphs about the workshop. **Leave an empty line between paragraphs.** The first paragraph is shown larger, in italics, so it works well for the part's voice (e.g. *"Just say yes. They'll be disappointed."*). | |
| **This is for you if…** | One line per item. Click **Add** for each new line. | You find it hard to say no |
| **What happens (in order)** | One step per item, with a short **Step** name and a **Description**. | Landing / We arrive, with a cup of coffee. |

Every workshop page automatically gets:
- the **Workshop** label at the top
- the "Everything is an invitation … not therapy" note
- the practical box with **Format: In person, sitting, everyday clothes, no touch**
- the buttons to ask about dates and to book it for a space or team
- the free 20-minute call link and your signature

## 4. Change or remove a workshop

- **Change:** open **Workshops**, click the workshop, edit, **Save**.
- **Remove:** open the workshop and delete the entry, then **Save**.
- **Add a date when you have one:** fill in **Next date and venue** and, if you like, **Price** and **Group size**. Change the status to *Open for sign-up*.

## 5. Good to know

- **The first workshop in the list is the main page.** The page at `/workshops.html` is *Coffee with Your Inner Critic*. Keep it at the top of the list. Its opening (the **Workshop** label, the title, *"Ever tried sitting down with your inner critic?"* and the crossed-out lines) is written into `workshops.html` itself. Its "for you", steps and practical details come from the CMS like the others.
- **Every other workshop has its own link:** `www.parts-work.dk/workshops.html#` + the web address. For example `www.parts-work.dk/workshops.html#people-pleaser`. Use that link when you share a workshop on social media or in emails.
- **Nothing in [square brackets] should ever be on the site.** Just leave a field empty if you don't have the information yet; empty fields are hidden.
- **If something looks broken** after saving, open the workshop in Pages CMS again and check for a missing title or web address. Every save is stored in GitHub, so any change can be undone (see *Undo a change* in the README).
