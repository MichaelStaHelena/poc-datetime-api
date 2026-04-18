# poc-datetime-api

A small Java **proof-of-concept (PoC)** project demonstrating common usage patterns of the **`java.time`** (JSR-310) Date/Time API: `LocalDate`, `LocalTime`, `LocalDateTime`, `Instant`, `ZonedDateTime`, `Duration`, `Period`, formatting/parsing, temporal adjusters, comparisons, and conversions to/from legacy `java.util.Date`.

## What’s inside

The project is primarily a runnable demo class:

- `src/main/java/com/michael/poc/Main.java` — contains multiple `example*()` methods showing practical `java.time` operations and logs the results.

Topics covered include:

- **Dates & times**: `LocalDate`, `LocalTime`, `LocalDateTime`
- **UTC timestamps**: `Instant`
- **Time zones**: `ZonedDateTime`, `ZoneId`, zone conversion (`withZoneSameInstant`)
- **Intervals**: `Duration` (time-based) and `Period` (date-based)
- **Formatting & parsing**: `DateTimeFormatter` (including custom patterns and locale examples)
- **Calendar navigation**: `TemporalAdjusters` (end of month, next Monday, etc.)
- **Comparisons & calculations**: `isBefore/isAfter`, `ChronoUnit.between`, age calculation
- **Legacy conversion**: `java.util.Date` ↔ `java.time`

## Requirements

- **Java 21**
- **Maven**

The Maven configuration compiles with Java 21 and sets the runnable main class to:

- `com.michael.poc.Main`

## Build

```bash
mvn clean package
```

## Run

Using the Maven exec plugin:

```bash
mvn exec:java
```

## Dependencies

- **Lombok** (provided) — for reducing boilerplate (e.g., `@Slf4j`)
- **SLF4J API + slf4j-simple** — logging
- **JUnit 5** — tests (API + engine)

## Notes

- Output is produced via SLF4J logging (info level).
- Several examples depend on the **system default time zone** at runtime (`ZoneId.systemDefault()`), so output may vary by machine.

## License

No license file is currently included in this repository.
