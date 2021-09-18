# locale-en-US

This repo contains the English language files for the State of JS/CSS/etc. surveys, which serve as a base to translate all the other languages. You can view a list of [all the locales repos here](https://github.com/StateOfJS/?q=locale-&type=&language=&sort=).

## Getting Credit

Every translator will be credited on any site that makes use of the translations, starting with the survey-taking app. You can add your name here if it's not already there.

- https://github.com/StateOfJS/state-of-js-graphql-results-api/blob/master/src/i18n/locales.yml

## Translation API

You can get extra data such as the completion percentage for a locale or the untranslated strings via our API, available at: 

- https://graphiql.stateofjs.com/

Here is a sample query: 

```graphql
query GetLocaleData {
  locale(localeId: "ru-RU") {
    completion
    totalCount
    translatedCount
    translators
    untranslatedKeys
  }
}
```

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

It's recommended you join the [translation team](https://github.com/orgs/StateOfJS/teams/translators/teams) for the language you want to translate.

## Local Development

There is currently no easy way to see your strings in context while developing locally. We are working on it. 

## Getting Help

Join [our Discord](https://discord.gg/zRDb35jfrt).
