# Read: 28 - RecyclerView

## What is a RecyclerView? 
- it is the ViewGroup that contains the views corresponding to your data. so you add RecyclerView into your layout the way you would add any other UI element.
- any item in the recycleview is defined by a view holder object.
- it is a list because The layout manager arranges the individual elements in your list.


## How to implement it ?

1- decide the look that the list or grid is going to look like. Ordinarily you'll be able to use one of the RecyclerView library's standard layout managers.

2- decide how each element in the list is going to behave. Based on this design, extend the ViewHolder class.

3- Define the Adapter that associates your data with the ViewHolder views.

## there are 3 layout managers, what are they?

- LinearLayoutManager arranges the items in a one-dimensional list.
- GridLayoutManager arranges all items in a two-dimensional grid:
    - If the grid is arranged vertically, GridLayoutManager tries to make all the elements in each row have the same width and height.
    - If the grid is arranged horizontally, GridLayoutManager tries to make all the elements in each column have the same width and height.
StaggeredGridLayoutManager is similar to GridLayoutManager, but it does not require that items in a row have the same height (for vertical grids) or items in the same column have the same width (for horizontal grids).

When you define your adapter, what are the  three key methods:

onCreateViewHolder(): RecyclerView calls this method whenever it needs to create a new ViewHolder. The method creates and initializes the ViewHolder and its associated View, but does not fill in the view's contents—the ViewHolder has not yet been bound to specific data.

onBindViewHolder(): RecyclerView calls this method to associate a ViewHolder with data. The method fetches the appropriate data and uses the data to fill in the view holder's layout. For example, if the RecyclerView displays a list of names, the method might find the appropriate name in the list and fill in the view holder's TextView widget.

getItemCount(): RecyclerView calls this method to get the size of the data set. For example, in an address book app, this might be the total number of addresses. RecyclerView uses this to determine when there are no more items that can be displayed.

