# *Tweet Away*

Tweet Away is an android app that allows a user to view his Twitter timeline. The app utilizes [Twitter REST API](https://dev.twitter.com/rest/public).

## User Stories

- [x] User can **sign in to Twitter** using OAuth login
- [x]	User can **view tweets from their home timeline**
  - [x] User is displayed the username, name, and body for each tweet
  - [x] User is displayed the [relative timestamp](https://gist.github.com/nesquena/f786232f5ef72f6e10a7) for each tweet "8m", "7h"
- [x] User can refresh tweets timeline by pulling down to refresh


- [x] User can view more tweets as they scroll with infinite pagination
- [x] Improve the user interface and theme the app to feel "twitter branded"
- [x] Links in tweets are clickable and will launch the web browser
- [x] User can tap a tweet to display a "detailed" view of that tweet
- [x] User can see embedded image media within the tweet detail view
- [x] On the Twitter timeline, leverage the CoordinatorLayout to apply scrolling behavior that hides / shows the toolbar.

- [x] User can **compose and post a new tweet**
  - [x] User can click a “Compose” icon in the Action Bar on the top right
  - [x] User can then enter a new tweet and post this to twitter
  - [x] User is taken back to home timeline with **new tweet visible** in timeline
  - [x] Newly created tweet should be manually inserted into the timeline and not rely on a full refresh
  - [x] User can **see a counter with total number of characters left for tweet** on compose tweet page

- [x] User is using **"Twitter branded" colors and styles**
- [x] User can click links in tweets launch the web browser 
- [x] The "Compose" action is moved to a FloatingActionButton instead of on the AppBar
- [x] Compose tweet functionality is build using modal overlay
- [x] Use Parcelable instead of Serializable using the popular [Parceler library](http://guides.codepath.org/android/Using-Parceler).
- [x] User can **open the twitter app offline and see last loaded tweets**. Persisted in SQLite tweets are refreshed on every application launch. While "live data" is displayed when app can get it from Twitter API, it is also saved for use in offline mode.

## Video Walkthrough

Here's a walkthrough of implemented user stories:

### Login and Home Timeline
<img src="walkthroughs/Portrait_twitter1.gif" width=250><br>

### Toolbar Collapse on Scroll
<img src="walkthroughs/Portrait_twitter2.gif" width=250><br>

### Swipe to Refresh
<img src="walkthroughs/Portrait_twitter3.gif" width=250><br>

### Clickable Links, Tweet Detail View, Embedded Media, Infinite Scroll!
<img src="walkthroughs/Portrait_twitter4.gif" width=250><br>

<img src="walkthroughs/Portrait_Twitter_Part2.gif" width=250><br>


## Notes

- Still working to get data persistence with Sql-Lite implemented.  Having trouble populating the user_id(foreign key) in the tweet entity
- Still working on embedded video media.  Struggling with 3rd party libraries.  Also, seems video media can still be labelled "photo" in the twitter API?  May have to use extended entities and search for "video" under type.  Seems videos still have a "photo" type in the simple media entity?

## Open-source libraries used

- [Android Async HTTP](https://github.com/codepath/CPAsyncHttpClient) - Simple asynchronous HTTP requests with JSON parsing
- [Glide](https://github.com/bumptech/glide) - Image loading and caching library for Android

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
