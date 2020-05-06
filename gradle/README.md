# GRADLE

## Documentation

https://gradle.org/

## Exemple de ligne utilisée

Nettoyage et build

```
./gradlew clean build
```

Sans les tests

```
./gradlew clean build -x test
```

Install de maven

```
./gradlew clean build -x test install
```

Trouver les dépendances

```
./gradlew dependencyInsight --dependency <JAR> :<REPO>
```

