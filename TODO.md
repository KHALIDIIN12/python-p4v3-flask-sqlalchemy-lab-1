# TODO List - Flask SQLAlchemy Lab

## Phase 1: Define Earthquake Model
- [ ] Define Earthquake model class in server/models.py
  - Inherit from db.Model and SerializerMixin
  - Set __tablename__ = "earthquakes"
  - Add id (int, primary key), magnitude (float), location (string), year (int) columns
  - Add __repr__ method returning format: <Earthquake 1, 9.5, Chile, 1960>
- [ ] Run tests to verify model: pytest testing/models_test.py

## Phase 2: Initialize Database
- [x] Run migrations: flask db init && flask db migrate -m "initial migration"
- [x] Apply migration: flask db upgrade head
- [x] Seed the database: python seed.py

## Phase 3: Add Views to app.py
- [x] Import Earthquake from models
- [x] Add /earthquakes/<int:id> route returning JSON or 404
- [x] Add /earthquakes/magnitude/<float:magnitude> route returning count and quakes list

## Phase 4: Test Everything
- [x] Run all tests: pytest (11 passed)
- [x] Run specific tests: pytest testing/app_earthquake_test.py (4 passed) and pytest testing/app_magnitude_test.py (3 passed)

## Phase 5: Git Commit
- [ ] Stage changes: git add .
- [ ] Commit: git commit -m "Complete Flask SQLAlchemy Lab"

