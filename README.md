Kitesurfing App for Android
===========================

The app implements succesfully the following features:
* Has **LIST**, **FILTER** and **DETAIL** activities
* Handles network-calls to different API endpoints
* **Handles network-call errors** and converts JSON files accordingly
* Activities handle screen rotations and **configuration changes** and **preserve information between states**
* Layout is **scalable and adaptable** to different screen sizes and densities
* Interface is highly intuitive and provides the user with meaningful screen messages
* Interface does not freeze as network operations are handled on a **background thread**

Implementation highlights:
* Network calls are made using [Retrofit](https://square.github.io/retrofit/) library along with [Okhttp](https://square.github.io/okhttp/)
* Responses from server are converted using the [Gson](https://github.com/google/gson) library
* The main list is handled for the layout using [RecyclerView](https://developer.android.com/guide/topics/ui/layout/recyclerview) 
* All strings, dimensions and colors used are **extracted in resource files**
* Communication between Activities is handled using `startActivityForResult()` method and `onActivityResult()` callback
* Different boolean variables are used in order to reduce the number of network requests and to prevent overlapping calls
* If no network operation is performed, current data is **cached between screen configuration changes**
* Used an `Intent` for opening a spot location on GoogleMaps 
