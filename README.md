# Quinn Ridgeway

## Posts:

### week 3:

**What did you do last week?**
I set up my leet code account, and looked at one problem. I also examined the largest human connectome dataset. It is to date the largest map of neural connections from an individual human brain ever produced. It has synapse level information and is the biggest publicly available brain map that I am aware of.   

**What do you plan to do this week?**
I want to examine the difficulty of simulating a small piece of the brain map with a graph representation.

**Are there any impediments in your way?**
A lack of information. I think it would be cool to simulate part of an actual human brain as a final project but this could be biting of more than I can chew. I will examine the difficulty more fully now and assess feasibility.

**Reflection on the process you used last week, how can you make the process work better?**
I plan on getting more organized, I got distracted working on other classes that I should have taken earlier on in my degree. 

### week 4:
  
**What I did  last week:**
Last week I decided to focus on leetcode for my project. I may still try to mess around with the human brain data on the side, but it was probably too much for one semester with other classes. It would be neat to have a graph representation of one human cortical mini-column by the end of the semester. 

**What do I plan to do this week:**
This week I plan to focus on getting my personal website set up. Once I have that I can start recording my leetcode progress in a digestible format. I also need to catch up on other classes to carve out time specifically dedicated to leetcode. 

**Are there any impediments in my way:** 
The main stumbling block I hit this week was distraction in other classes. I took the first computer systems midterm this week and studying for that occupied the majority of my time. 

**Reflection on the process used last week, and how can I make the process work better:**
I think that my main goal should be to get caught up in all other classes so that I can schedule a dedicated day for leetcode/ brain analysis. I have also heard that when first starting in leetcode it's wise to memorize some fundamental algorithms and patterns, so that all of your cognitive effort can be focused on permuting them into a specific solution. I started with binary search, and I think I have it mostly memorized. 

### week 5:
 
**What did you do last week?**
Last week I worked on memorizing a few fundamental algorithms for leetcode problems. I have been focusing mainly on binary search problems.

**What do you plan to do this week?**
This week I need to finish my website and continue working on binary search problems. I think I have it pretty much down. I am also going to look at the cortical minicolumn data in the free brain data website. 

**Are there any impediments in your way?**
My main impediment this week is remaining on top of computer systems. So far it has turned out ok but the volume of information is rather large. I also will need to work a decent amount this weekend.

**Reflection on the process you used last week, how can you make the process work better?**
I think continuing to schedule will be the most important thing to focus on. I have found that merely starting things early and not necessarily completing them fully gives you much more momentum.

### week 7:

**What did you do last week?**
Last week I prepared for exam two in computer systems and looked into some graph theory stuff when considering cortical columns. I also looked into depth first search more thoroughly for leetcode. I haven't fully memorized it yet but will keep working on that. I also had to turn in the first machine learning project in that class which took quite a while.

**What do you plan to do this week?**
This week I needed to prepare more for exam two in computer systems, which was very time consuming. I also miss-read the timing of the exam and took it in the middle of the night so as not to entirely miss the exam. This week I also need to finish one of the computer systems labs which I anticipate to be difficult.

**Are there any impediments in your way?**
I am getting better at scheduling but it is still difficult to prioritize making real gains on the brain simulation. I think by next week I will have much more time to focus on leetcode progress/ the brain. There appears to be a lull in the intensity of my other two classes in week eight.

**Reflection on the process you used last week, how can you make the process work better?**
I think my best strategy is going to be finding a specific day this upcoming week to solely dedicate to my goals in this class. As a side note I have included the link to the brain dataset, it is 1.4 petabytes, which is crazy! https://h01-release.storage.googleapis.com/landing.html 


## Fundamental Algorithms for Leetcode:
  
### Binary Search
```python
     def binarySearch(arr, low, high, x):
       while low <= high:
         mid = low + (high - low) // 2
        
         # Check if x is present at mid
         if arr[mid] == x:
           return mid

         # If x is greater, ignore left half
         elif arr[mid] < x:
           low = mid + 1

         # If x is smaller, ignore right half
         else:
           high = mid - 1

       # If we reach here, then the element
       # was not present
       return -1
  ```
  Source: https://www.geeksforgeeks.org/binary-search/

  
### DFS
```python
     def add_edge(adj, s, t):
       # Add edge from vertex s to t
       adj[s].append(t)
       # Due to undirected Graph
       adj[t].append(s)


     def dfs_rec(adj, visited, s):
      # Mark the current vertex as visited
       visited[s] = True

       # Print the current vertex
       print(s, end=" ")

       # Recursively visit all adjacent vertices
       # that are not visited yet
       for i in adj[s]:
         if not visited[i]:
           dfs_rec(adj, visited, i)


     def dfs(adj, s):
       visited = [False] * len(adj)
        # Call the recursive DFS function
        dfs_rec(adj, visited, s)


     if __name__ == "__main__":
        V = 5

       # Create an adjacency list for the graph
        adj = [[] for _ in range(V)]

        # Define the edges of the graph
        edges = [[1, 2], [1, 0], [2, 0], [2, 3], [2, 4]]

        # Populate the adjacency list with edges
        for e in edges:
        add_edge(adj, e[0], e[1])

       source = 1
       print("DFS from source:", source)
       dfs(adj, source)
  ```
  source: https://www.geeksforgeeks.org/depth-first-search-or-dfs-for-a-graph/

  
### BFS
  

## Cortical Minicolumn:

### Under Construction

<picture>
 <source media="(prefers-color-scheme: dark)" srcset="https://upload.wikimedia.org/wikipedia/commons/2/21/Cortical_Minicolumn.png">
 <source media="(prefers-color-scheme: light)" srcset="https://upload.wikimedia.org/wikipedia/commons/2/21/Cortical_Minicolumn.png">
 <img alt="Cortical Minicolumn in mouse cortex" src="https://upload.wikimedia.org/wikipedia/commons/2/21/Cortical_Minicolumn.png">
</picture>


