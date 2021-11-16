# RecyclerView

## Create dynamic lists with RecyclerView

- RecyclerView makes it easy to efficiently display large sets of data. You supply the data and define how each item looks, and the RecyclerView library dynamically creates the elements when they're needed.

- RecyclerView recycles those individual elements. When an item scrolls off the screen, RecyclerView doesn't destroy its view. Instead, RecyclerView reuses the view for new items that have scrolled onscreen.

### **[Key classes]**

- RecyclerView is the ViewGroup that contains the views corresponding to your data.

- Each individual element in the list is defined by a view holder object.

- The RecyclerView requests those views, and binds the views to their data, by calling methods in the adapter.

- The layout manager arranges the individual elements in your list.

### **[Steps for implementing your RecyclerView]**

<br>

**First of all, decide what the list or grid is going to look like ---> Design how each element in the list is going to look and behave ---> Define the Adapter that associates your data with the ViewHolder views.**

<br>

### **[Plan your layout]**

most common layout situations:

- `LinearLayoutManager` arranges the items in a one-dimensional list.

- `GridLayoutManager` arranges all items in a two-dimensional grid.

- `StaggeredGridLayoutManager` is similar to GridLayoutManager, but it does not require that items in a row have the same height or items in the same column have the same width.

### **[Implementing your adapter and view holder]**

Once you've determined your layout, you need to implement your Adapter and ViewHolder. These two classes work together to define how your data is displayed. The ViewHolder is a wrapper around a View that contains the layout for an individual item in the list.
