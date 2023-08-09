# KX Dashboards Post

In order to replicate this post's dashboard on your machine, there are a couple of things needed:

* The dataset must be served on a q session running on port 5001. This can be done by executing `\p 5001` on a q session. It'is available [here](https://drive.google.com/file/d/1mvSi7-EwIwUYR7Yjtajk56rg5eLWSBo-/view?usp=drive_link) both as the 12 million row table and a smaller, more compact 1 million row table. Whichever you choose to use, it should be saved as a table in memory on this said q process with the name **complete**. The q code to read and save this table with the proper meta is the following (change the file name if needed):

```q
complete:("PJJJFFFFFFFFFFDT";enlist ",")0:`$":complete.csv"
```

* A [Google Maps API Key](https://developers.google.com/maps/documentation/javascript/get-api-key) for the map component.

* KX Dashboards installed on your system. Instructions are available [here](https://code.kx.com/dashboards/gettingstarted/). We recommend installing it either on a Linux system or [WSL](https://learn.microsoft.com/en-us/windows/wsl/install).

The dashboard itself is provided as a JSON file on this post's [Github Repository](https://github.com/hablapps/kx-dashboards-post), inside the `source` folder. To make it available on the web interface, it needs to be placed on the directory `dash/data/dashboards` on the KX Dashboards installation directory.

If you wish to build the dataset from scratch, we strongly recommend you follow our [posts on PyKX](https://github.com/hablapps/AllRoadsLeadToPyKX/), where we get the source data files and work with them to ultimately obtain this very table we need. We also recommend to give them a read whenever possible to understand the context of this post.

The post assumes everything described here is ready and working.

This is the final dashboard we managed to build:

![](images/19-final-result.png)