Use kebab-case for keys in aplication.yml.

Use the key word var in init variables.

DB work layer must have dao package and Dao in suffix.

Web:
- Controllers place in controlle package.
- Use static html/css/js and place in resources.

All models place in model package, with additional subpackages.

Stack: Java 21, Gradle, Micronaut, Jdbi, for telegram - rubenlagus/TelegramBots, Flyway, Postgres.

Telegram:
- Use only webhook handler with /webhook path

Add logback.xml and add configs that i can only specify log level if i need it

Add gradle wrapper in root and ./gradlew

