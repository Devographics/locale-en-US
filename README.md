# locale-en-US

This repo contains the English language files for the State of JS/CSS/HTML/etc. surveys, which serve as a base to translate all the other languages. You can view a list of [all the locales repos here](https://github.com/orgs/Devographics/repositories?q=locale-&type=all&language=&sort=name).

## How To Help

#### 1. Becoming a Translator

To start helping translate the survey, you should [join the Discord](https://discord.com/invite/zRDb35jfrt) and DM me (`SachaG`) your GitHub username, along with the locale code (`fr-FR`, `zh-Hant`, etc.) for the language you'd like to help with.

I will then give you maintainer rights over a repo containing all the translation `yaml` files, and from now on you can manage it yourself along with other members of the translation team.

#### 2. Finding Things to Translate

You can either browse the survey-taking app, survey results site, etc. and find untranslated strings this way, or else use our API to get extra data such as the completion percentage for a locale or a list of all the untranslated strings:

- https://graphiql.devographics.com/

Here is a sample query:

```graphql
query GetLocaleData {
  locale(localeId: ru_RU) {
    completion
    totalCount
    translatedCount
    translators
    untranslatedKeys
  }
}
```

#### 3. Getting Credit

Every translator will be credited on any site that makes use of the translations, starting with the survey-taking app. In order to receive credit, add your GitHub username to the `translators` array in each locale's `config.yml` file.

Here is an example for the `de-DE` locale:

- https://github.com/Devographics/locale-de-DE/blob/main/config.yml#L3

#### 4. Pushing Your Changes Live

There is currently no automated hook to update the production apps when a translation is updated, so for now the best way is to DM me on Discord to let me know when you're finished.

## Translation Files

#### Surveys App

These strings are related to the app that you use to fill out the actual survey.

- `surveys.yml`
- `accounts.yml`
- `state_of_js_2020_survey.yml`

#### Results App

These strings only appear in the static site that displays the survey results and stats.

- `results.yml`
- `state_of_css_2020.yml`
- `state_of_js_2020.yml`

#### Both

These strings appear in both.

- `common.yml`
- `state_of_css.yml`
- `state_of_js.yml`

#### Other

- `homepage.yml`

## Joining Translation Teams

It's recommended you join the [translation team](https://github.com/orgs/Devographics/teams/translators/teams) for the language you want to translate.

## Local Development

There is currently no easy way to see your strings in context while developing locally. We are working on it.

## Getting Help

Join [our Discord](https://discord.gg/zRDb35jfrt).
