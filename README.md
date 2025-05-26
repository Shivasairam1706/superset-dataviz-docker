✨ Superset Data Visualization Stack - Powered by Docker 🚀

Welcome to your launchpad for building beautiful, interactive dashboards with Apache Superset, fully containerized for convenience and speed. Whether you're a data enthusiast, analyst, or engineer, this stack gets you from zero to visualization hero in minutes.

📊 What Is This?

This project is a custom Superset deployment bundled with:

PostgreSQL — for storing metadata

Redis — for caching and session handling

Superset (Custom Image) — extended with essential Python packages like pandas, pyarrow, and more

Ideal for:

Data visualization projects

Dashboard prototyping

Personal analytics playgrounds

🚧 Quick Launch

1. Clone This Repo

git clone https://github.com/<your-username>/superset-dataviz-docker.git
cd superset-dataviz-docker

2. Set Your Secrets

Edit the .env file:

POSTGRES_DB=superset
POSTGRES_USER=admin
POSTGRES_PASSWORD=Iamsuperman5433
SUPERSET_ADMIN_PASSWORD=Iamsuperman5433
SECRET_KEY="YourRandomSecretKeyHere"

3. Fire It Up ✨

docker-compose up --build

Once running, visit: http://localhost:8085

Login credentials:

Username: admin

Password: Iamsuperman5433

🌐 What's Inside?

.
├── docker-compose.yml             # Orchestrates Superset, Redis, Postgres
├── Dockerfile                     # Custom Superset image with extra Python libs
├── requirements.txt              # Python dependencies
├── .env                          # Your secrets (excluded from Git)
├── docker-init/
│   └── superset_bootstrap.sh     # Auto-setup: DB migrate, admin user, init
├── superset_config/
│   └── superset_config.py        # Custom Superset configurations

✨ Features

✅ Out-of-the-box Superset setup

🧵 Redis caching & session storage

🎓 PostgreSQL metadata backend

📆 Custom config with modern feature flags

🚜 Easily extensible with Python packages

🌟 Ideal for personal or team-based analytics workflows

🔍 Notable Configs

superset_config.py

Enables CSV uploads, drag & drop UI, advanced datatypes

Configures Redis as Flask cache + session backend

superset_bootstrap.sh

Waits for Postgres to be ready

Initializes database

Creates admin user

Starts the Superset server

🔔 Pro Tips

Use Docker volumes to persist metadata and dashboards

Customize requirements.txt to supercharge Superset

Add .env to .gitignore to keep secrets private

📅 License

MIT License. Use freely and build awesome dashboards!

🚀 Ready to Visualize?

Just run docker-compose up, log in, connect your datasets, and start creating dashboards that make your data speak volumes!

Because good data deserves great visuals. ✨

