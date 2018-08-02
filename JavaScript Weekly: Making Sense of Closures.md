# A brief review of scope

## Scope is composed of a set of nested boundaries that define which variables are accessible at any given point in your code

# Simple closure

```javascript
var event = "Coffee with Ada.";

function describeEvent() {
  console.log(event);
}

function calendar() {
  var event = "Party at Charles' house.";

  describeEvent();
}

calendar();               // Logs: "Coffee with Ada."

```

# Closure in high-order functions

```javascript
function makeEventDescriber(event, date) {
  return function() {
    console.log(date + ": " + event);
  };
}

var coffeeWithAda = makeEventDescriber("Coffee with Ada.", "8/1/2018");
var partyAtCharles = makeEventDescriber("Party at Charles' house.", "8/4/2018");

coffeeWithAda();          // Logs: "8/1/2018: Coffee with Ada."
partyAtCharles();         // Logs: "8/4/2018: Party at Charles' house."
```

# Fun with partial function application

```javascript
function schedulerMaker(name) {
  return function(event) {
    return function() {
      console.log(event + " with " + name + ".");
    };
  };
}

var adaScheduler = schedulerMaker("Ada");
var coffeeWithAda = adaScheduler("Coffee");

coffeeWithAda();          // Logs: "Coffee with Ada."
```

# Private data and application interfaces

## two of the biggest benefits of closure are the ability to create private data and to define application interfaces

```javascript
function makeCalendar(name) {
  var calendar = {
    owner: name,
    events: [],
  };

  return {
    addEvent: function(event, dateString) {
      var eventInfo = {
        event: event,
        date: new Date(dateString),
      };
      calendar.events.push(eventInfo);
      calendar.events.sort(function(a, b) {
        return a.date - b.date;
      });
    },

    listEvents: function() {
      if (calendar.events.length > 0) {
        console.log(calendar.owner + "'s events are: ");

        calendar.events.forEach(function(eventInfo) {
          var dateStr = eventInfo.date.toLocaleDateString();
          var description = dateStr + ": " + eventInfo.event;

          console.log(description);
        });
      } else {
        console.log(calendar.owner + " has no events.");
      }
    },
  };
}

var babbageCalendar = makeCalendar("Charles Babbage");

babbageCalendar.addEvent("Coffee with Ada.", "8/7/2018");
babbageCalendar.addEvent("Difference Engine presentation.", "8/2/2018");

babbageCalendar.listEvents();
  /*
    Logs:
    Charles Babbage's events are:
    8/2/2018: Difference Engine presentation.
    8/7/2018: Coffee with Ada.
  */
  ```

