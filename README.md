# RaceTracker

* A Vue web app using Firebase to track racers at an event.

### JS Components
Header
* Menu
  * Races
  * Login
  * About
  * Time Logging (Conditionally show on login)
Race List Page
* Race List 
  * Race List Item
    * Title
    * Description
    * Start Date
    * End Date
Race Event Page
* Map
  * Google map to show :
    * Race event and each checkpoint.
    * Racers along the race
* Standings List
  * Filterable via collapsible search input filter to search for a racer
  * Standing List Item
    * Racer Name
    * Racer position
    * Checkpoint List collapsible accordion
      * Checkpoint List Item
        * Name
        * Time
Time Logging
* Form (Create/Edit)
  * Autocomplete select list of Racers
  * Autocomplete select list of Checkpoints
  * Select List
    * Enter
    * Exit
  * Time
Login Page
* Form
  * Username
  * Password

### Services
* VueX to manage state
* Firebase for authentication and hold race event data

### Data Structure
Race Event
* String uuid
* String Title
* String Description
* DateTime Start date and time
* DateTime End date and time
* String Location (Coordinates)
* Array Racers
* Array Checkpoints
Racer
* String uuid
* String Name
* DateTime Event Time
* Checkpoint[] Checkpoint enter time
* Checkpoint[] Checkpoint exit time
* Race Event[] Races
  * Races can be subscribed to multiple races
Checkpoint
* String uuid
* String Title
* String Location (Coordinates)
* Int Race ID
  * A checkpoint can only be assigned to one race
User
* String uuid
* String Name
* String Email
* String[] Permissions
