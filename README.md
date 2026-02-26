# Bruin Pipeline Quiz — Answers & Explanations

## Question 1. Bruin Pipeline Structure

**Answer:** `.bruin.yml and pipeline/ with pipeline.yml and assets/`
**Explanation:** A Bruin project requires a root `.bruin.yml` config file and a `pipeline/` directory containing `pipeline.yml` and the `assets/` folder.

---

## Question 2. Materialization Strategies

**Answer:** `time_interval - incremental based on a time column`
**Explanation:** The `time_interval` strategy processes data for a specific time window by deleting and re-inserting records for that period.

---

## Question 3. Pipeline Variables

**Answer:** `bruin run --var 'taxi_types=["yellow"]'`
**Explanation:** Array variables must be passed in valid JSON format when overriding from the CLI.

---

## Question 4. Running with Dependencies

**Answer:** `bruin run ingestion/trips.py --downstream`
**Explanation:** The `--downstream` flag runs the modified asset plus all assets that depend on it.

---

## Question 5. Quality Checks

**Answer:** `name: not_null`
**Explanation:** The `not_null` check ensures a column never contains NULL values.

---

## Question 6. Lineage and Dependencies

**Answer:** `bruin lineage`
**Explanation:** The `lineage` command visualizes the dependency graph between pipeline assets.

---

## Question 7. First-Time Run

**Answer:** `--full-refresh`
**Explanation:** The `--full-refresh` flag rebuilds tables from scratch, which is useful for the first execution on a new database.

---
