# Django + Elasticsearch Integration

This repository demonstrates how to integrate **Elasticsearch** with **Django REST Framework (DRF)** for powerful full-text search capabilities. The implementation is inspired by the [TestDriven.io guide](https://testdriven.io/blog/django-drf-elasticsearch/).

---

## 🚀 Features

* Full-text search with **Elasticsearch**.
* Seamless integration with **Django ORM**.
* REST API endpoints using **Django REST Framework**.
* Search indexing and filtering support.
* Built with **elasticsearch-dsl** for flexible queries.

---

## 🛠️ Tech Stack

* **Backend:** Django, Django REST Framework
* **Search Engine:** Elasticsearch
* **Python Client:** elasticsearch-dsl
* **Database:** SQLite (can be switched to PostgreSQL/MySQL)

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
source venv/bin/activate   # On Linux/Mac
venv\Scripts\activate      # On Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Start Elasticsearch

Make sure you have Elasticsearch running locally. You can use Docker:

```bash
docker run -d --name elasticsearch \
  -p 9200:9200 \
  -e "discovery.type=single-node" \
  docker.elastic.co/elasticsearch/elasticsearch:7.17.9
```

### 5. Apply migrations

```bash
python manage.py migrate
```

### 6. Build search index

```bash
python manage.py search_index --rebuild
```

### 7. Run the server

```bash
python manage.py runserver
```

---

## 🔎 Example Usage

* Visit API root: `http://127.0.0.1:8000/api/`
* Use the search endpoint:

  ```http
  GET /api/search/?q=example
  ```

---

## 📂 Project Structure

```
.
├── app/                  # Django app with models and search integration
├── config/               # Django project settings
├── requirements.txt
├── manage.py
└── README.md
```

---

## 📖 References

* [Django + Elasticsearch + DRF Guide](https://testdriven.io/blog/django-drf-elasticsearch/)
* [Elasticsearch Docs](https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html)
* [Django REST Framework](https://www.django-rest-framework.org/)

---

## 📝 License

This project is licensed under the MIT License.
