# Arbetsprov Tele2: primevue-test

This project was created as a coding test for Tele2.

## Features
### Existing Features
The project consists of a form element with:
* A text input asking for full name
* A text input asking for owner
* A dropdown cascade select element asking for status between options:
   * Constructed
   * Initiated 
  Both accompanied by child elements:

**Constructed:**
* Constructed
* Frozen
* Planned for Termination
* Termination Ordered

**Initiated**
* Initiated 
* Accepted 
* Rejected
* Cancelled

* A dropdown element asking for Network Functions between options:
  * Switching: BNG, CG-NAT, routers
  * Tunnelling gateway elements: IPSec/SSL VPN gateways
  * Traffic analysis: DPI, QoE measurementI
  * Signalling: SBCs, IMS

* A dropdown element asking for Placement between options:
  * Stockholm
  * Göteborg
  * Malmö
  * Kiruna

* A editable dropdown element asking for Aliases with options:
  * AA77
  * AB35
  * CB56
  * LL89
  * TT78

* A larger text input area asking for directions
* A create button which when clicked displays a success toast message

### Features left to implement
Because of time restraints I was unable to properly implement some of the features, I aim to complete these on my own time when grading is completed. The features are:
* To separate the dropdown field for status and substatus into two separate dynamic dependent dropdowns instead of one single dropdown cascade element like requested in the instructions.
* To attach the required attribute to all dropdown elements, currently only text fields are required.  
* To fix the success toast message that shows up when clicking the *Create* button, currently the success message shows up regardless if the form is complete or not. 

## Acknowledgements
This is my first experience with working with Vue, I can see the appeal and the pros of the framework and I look forward to expanding my knowledge and getting more familiar as well as efficient with it.
