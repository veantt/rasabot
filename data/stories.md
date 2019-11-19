## happy path
* greet
  - utter_greet
* mood_great
  - utter_happy

## sad path 1
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* affirm
  - utter_happy

## sad path 2
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* deny
  - utter_goodbye

## say goodbye
* goodbye
  - utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot

## User want to see main menu
* greet
  - utter_greet
* want_main_menu
  - utter_show_main_menu
* select_menu
  - utter_confirm_main_menu

## Just want to see main menu
* want_main_menu
  - utter_show_main_menu
* select_menu
  - utter_confirm_main_menu
