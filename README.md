# JiJan (Jadwal & Jajan)

A website for managing your class schedule and daily pocket money together.

## Team

**Team name:** FX Flow

Muhammad Athallah Aziz, Coding in JavaScript & HTML<br>
Axel Basith Valentino, Coding in HTML<br>
Faraz Satria Nugraha & Aaron Elisha Sinulingga, Creative Design & Quality Assurance<br>


## Description

A lot of students end up impulse-buying snacks or eating out during long breaks between morning and afternoon classes, because that free time isn't planned. JiJan links a student's class schedule to their daily spending limit, so they can see their schedule and how much money they have left in one place.

### Main features

- **Daily class schedule.** Add and delete classes (subject, time, room). The class that's currently happening gets highlighted.
- **Gaps-between-classes planner.** If a break is 90 minutes or longer, JiJan shows a warning along with free or cheap study spots and cheap places to eat around campus. Food places that cost more than what's left of the day's budget are crossed out.
- **Pockets by schedule.** Each day can have its own spending limit, e.g. a bigger one for busy campus days and a smaller one for days at home.
- **Quick expense log.** Pick a category (Food, Transport, Academic, Hangout), enter the amount (with quick buttons for 5,000 / 10,000 / 15,000 / 25,000), add a note, and choose the payment method (cash or QRIS/e-wallet).
- **End-of-day reflection.** The "Tutup hari" (close the day) button shows whether the day's spending stayed under the limit, a breakdown per category, a streak of on-budget days, and a weekly spending chart. After 8 PM, the reflection pops up on its own once a day.

All data is saved in the browser, so it stays after a page refresh. When the site is opened for the first time it's completely empty, and users fill in their own schedule and budget.

Do note: the website's interface is in Indonesian.

## Technologies

- Plain HTML, CSS, and JavaScript (no framework)
- Browser `localStorage` for saving data
- [Chart.js](https://www.chartjs.org/) 4.4.1 for the weekly chart

This project is **front-end only**. There is no back end, server, or database.

## How to run

Nothing needs to be installed.

1. Download or clone this project folder.
2. Open `index.html` in a browser (Chrome, Edge, or Firefox).

Make sure you're connected to the internet so Chart.js and the fonts can load.

If you'd rather use a local server (optional), you can use the Live Server extension in VS Code, or run this from the project folder:

```bash
npx http-server -p 5500
```

then open http://localhost:5500.

### File structure

```
index.html   main page and all popups
styles.css   styling
main.js      app logic
data.js      list of days, categories, and places around campus
assets/      icons
```


## Templates, starter code, and third-party assets

- No templates or starter code were used.
- **AI (Claude)** was used for assisting to most math related functions and in the making of this `README.md`.
- **Chart.js** 4.4.1, loaded from the jsDelivr CDN (MIT License).
- **Google Fonts:** Fraunces, Work Sans, JetBrains Mono (SIL Open Font License).
- **Icons** `assets/Time.png`, `assets/Pig.png` (Source from Google Images)

## Additional notes and limitations

- Data is only stored in the browser being used. Switching browsers or devices, using incognito mode, or clearing browser data will lose it.
- There's no login and no syncing between devices.
- The study spots and food places in `data.js` are examples and aren't taken from real campus data. They can be swapped out to match any campus.
- Expenses are saved by date within the current week. Picking a day at the top shows that day of the current week; previous weeks can't be viewed yet.
- The 8 PM reflection reminder only appears if the website is open (no push notifications yet).
- There's no check yet for two classes with overlapping times.
- The "hapus semua data" (delete all data) button at the bottom of the page deletes every schedule and expense.
