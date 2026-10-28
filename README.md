# Django Monthly Challenges

A lightweight and efficient web application built with the Django web framework that dynamically tracks personal development goals, fitness milestones, and self-improvement routines for every month of the year.

## 🎯 Features

- **Dynamic Routing:** Utilizes absolute URL routing and custom parameter converters (`<str:month>` and `<int:month>`) to dynamically capture URL requests and map them to their corresponding dashboard cards.
- **Auto-Redirect Utility:** Includes integer-to-string path handlers using Django's native `HttpResponseRedirect` and `reverse` functions (e.g., navigating to `/challenges/1` automatically redirects to `/challenges/january`).
- **Comprehensive Annual Program:** Built-in memory structure housing uniquely tailored monthly workflows across fitness, learning (Django deep dives), lifestyle adjustments, and professional reflections.
- **Custom Error Handling:** Fully responsive, fail-safe architecture tracking invalid path configurations or unknown parameters to trigger strict `Http404` exceptions automatically.

## 🛠️ Tech Stack

- **Backend:** Python 3.14+, Django 6.0+
- **Frontend:** HTML5, CSS3, Django Template Language (DTL)
- **Routing Engine:** Django URL Resolver Architecture

## 📁 File Structure Overview

```text
monthly_challenges/
 │
 ├── challenges/             # Primary application workspace
 │    ├── static/            # Stylesheets and visual assets
 │    ├── templates/         # HTML template layouts (base, index, detail view)
 │    ├── views.py           # Core logic handling dictionaries and redirects
 │    └── urls.py            # Local routing path schemas
 │
 ├── amisner/                # Main project configuration tier
 │    ├── settings.py        # Global environment settings
 │    └── urls.py            # Master URL routing table (includes application paths)
 │
 └── manage.py               # Django execution management program
```

## 🚀 Installation & Local Setup

Follow these steps to get the development environment running locally.

### 1. Clone the Repository
```bash
git clone https://github.com
cd monthly_challenges
```

### 2. Set Up a Virtual Environment (Recommended)
```bash
python -m venv venv
# Activate on Windows:
venv\Scripts\activate
# Activate on macOS/Linux:
source venv/bin/activate
```

### 3. Start the Server
Since this app works entirely out of dynamic dictionary engines and memory matrices, you can immediately fire up your local developer instance:
```bash
python manage.py runserver
```

### 4. Testing Your Application Endpoints
Open your browser and test your active paths:
- **Main List:** `http://127.0.0`
- **Named Target:** `http://127.0.0march/` *(Loads March goals)*
- **Numerical Route:** `http://127.0.03/` *(Instantly redirects to `/challenges/march/`)*
