## chitchat
* chitchat
  - utter_default

## new rasa user 1
* greet
  - utter_greet
* name{"name":"Alice"}
  - utter_ask_location
* location{"location":"New York"}
  - utter_used_rasa
* deny
  - utter_docs

## existing rasa user 1
* greet
  - utter_greet
* name{"name":"Tom"}
  - utter_ask_location
* location{"location":"Berlin"}
  - utter_used_rasa
* affirm
  - utter_send_blog
* subscribe
  - action_subscribe
* goodbye
  - utter_goodbye

## existing rasa user 2
* greet
  - utter_greet
* name{"name":"Ben"}
  - utter_ask_location
* location{"location":"London"}
  - utter_used_rasa
* affirm+subscribe
  - utter_send_blog
  - action_subscribe
* deny
  - utter_goodbye

## existing rasa user 3
* greet
  - utter_greet
* name{"name":"Arthur"}
  - utter_ask_location
* location{"location":"Brasil"}
  - utter_used_rasa
* affirm+subscribe
  - utter_send_blog
  - action_subscribe
* goodbye
  - utter_goodbye

## new rasa user 2

* greet
    - utter_greet
* name{"name":"Alan"}
    - utter_ask_location
* location{"location":"London"}
    - utter_used_rasa
* deny
    - utter_docs
* thanks
    - utter_goodbye

## usual flow followed by thank you

* greet
    - utter_greet
* name{"name":"Jimbo"}
    - slot{"name":"Jimbo"}
    - utter_ask_location
* location{"location":"SF"}
    - slot{"location":"SF"}
    - utter_used_rasa
* affirm
	- utter_send_blog
* thanks
    - utter_goodbye

## Story from conversation with b9525ab7-2f36-4f9e-8385-44e8f783eaf5 on December 17th 2019

* greet
    - utter_greet
* name{"name":"Bob"}
    - slot{"name":"Bob"}
    - utter_ask_location
* location{"location":"San Francisco"}
    - slot{"location":"San Francisco"}
    - utter_used_rasa
* deny
    - utter_docs
    - slot{"name":"Bob"}
    - slot{"location":"San Francisco"}
    - utter_goodbye
