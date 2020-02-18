Based on the xAPI Video Profile and the xAPI Audio Profile we can create Statement Templates for listing to podcast episodes from a web page player.

* Experienced: Learner visited the page
* Started:  Learner started audio file
* Paused: Learner stopped audio file
* Stopped: Learner stopped audio file
* Completed: Learner completed audio file

We may also add statement templates for podcast related events like subscribe or unsubscribe to a podcast. We may leverage data from the Podcast RSS XML files and decide what data needs to be used in a statement (most likely as extensions).

**Experienced Statement (Draft, needs review):**

```
{
  "actor": {
    "name": "Oliver",
    "account": {
      "anonym": "http://github.com/xapicohort"
    }
  },
  "verb": {
    "id": "http://adlnet.gov/expapi/verbs/experienced",
    "display": {
      "en-US": "experienced"
    }
  },
  "object": {
    "id": "http://test",
    "definition": {
      "name": {
        "en-US": "Test Title"
      },
      "description": {
        "en-US": "Test Description"
      },
      "type": "https://w3id.org/xapi/video/activity-type/video"
    },
    "objectType": "Activity"
  },
  "context": {
    "contextActivities": {
      "category": {
        "id": "https://w3id.org/xapi/video"
      }
    },
    "extensions": {
      "http://xapicohort.github.io/xapi/activities/type": "podcast",
      "http://xapicohort.github.io/xapi/activities/url": "http://test"
    },
    "revision": "1"
  },
  "result": {
    "success": false,
    "completion": true,
    "extensions": {
      "https://w3id.org/xapi/video/extensions/progress": 1
    }
  },
  "version": "1.0.3",
  "id": "c242f3ca-ac8a-4f89-9580-a212422feaf4",
  "timestamp": "2020-02-18T22:23:44.887+00:00"
}
```


