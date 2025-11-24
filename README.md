# TfL Kings Cross Live Transport Dashboard

This project turns Transport for London’s messy, real-time data into a clear live dashboard focused on Kings Cross and nearby routes.

I built it during the **APIs to OMG** workshop with **Coding Black Females** at **Monzo Bank HQ**, led by **Marie Cruz (Grafana Labs)**. In a single afternoon I went from staring at raw JSON to a working observability-style view of London transport.

---

## 🎯 What this dashboard does

- Shows **live bus arrivals** for routes around Angel, Euston and Kings Cross.
- Shows **live tube arrivals** and line statuses (Metropolitan, Northern, Piccadilly, Victoria, etc.).
- Highlights **current TfL disruptions** and partial closures.
- Includes a **Kings Cross hourly summary panel**, written during my lunch break before heading to an event at Kings Cross.

The goal was to turn chaotic transport data into something calm, readable and decision-friendly.

---

## 🔧 Tech stack

- **Grafana** (visualisation and dashboarding)
- **Infinity plugin** (connecting HTTP API data directly to Grafana)
- **TfL Unified API** (live transport data)
- **jq & Grafana transformations** (shaping JSON into usable tables and status panels)

---

## 🧠 What I learned

- How to pull live API data straight into Grafana using the Infinity plugin.
- How to use **jq** and **transformations** to turn raw JSON into:
  - Arrival tables
  - Line status panels
  - Disruption summaries
- How to structure panels so that a user can quickly answer:
  - “Is my line running?”
  - “How bad is the disruption?”
  - “When is the next train or bus?”

This reinforced how much I enjoy taking messy data and turning it into something clear and useful, which is core to how I think about Product and Client Services roles.

---

## 👥 Collaboration

I built this dashboard as part of a collaborative workshop with:

- **Sumaya Kahie**
- **Regina Osei-Bonsu**

We helped each other:
- debug queries,
- test different ways of presenting the data,
- and iterate on panel layout and colours.

It felt like the right mix of learning, problem solving and laughing at our own debugging fails.

---

## 🧩 Product thinking

From a product perspective, this dashboard explores:

- **User problem**: TfL info is fragmented across apps, station boards and announcements.
- **Solution**: A single glanceable view showing status, arrivals and disruptions for one key hub (Kings Cross) and nearby routes.
- **User outcome**: Faster decisions about when to leave, what route to take and whether disruptions are serious enough to change plans.

If I had more time, future iterations could include:

- Personalised views by **home station** or **commute route**.
- Mobile-first layout with only the most critical panels.
- Alerts for “severe delays” or “no service” on favourite lines.

---

## 📸 Screenshots

![TfL Kings Cross Dashboard](assets/grafana-tfl-dashboard.png)

---

## 🏁 How to reuse or extend this

1. Import `dashboards/kings-cross-tfl-dashboard.json` into your Grafana instance.
2. Set up **Infinity** with your own TfL API key.
3. Update the station IDs, routes or panels to match your commute or city.

---

## 🙌 Credits

- **Coding Black Females** for organising the workshop.
- **Monzo** for hosting at their London HQ.
- **Marie Cruz (Grafana Labs)** for teaching the session and showing how to work with Infinity and jq.
- **Transport for London** for the open API.
