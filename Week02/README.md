学习笔记

广度搜索思路

1. find path function
    * create queue object
        > create an object to store pre path  
        > created by new Sorted object;  
        > pass in specific compare function;  
    * insert (go in)
        > deal with edge cases: reach border || already filled in;    
        > optional color marker  
        > store the pre location of current point (this will be used to track the best way)  
        > insert current location with give 
    * prepare for compare function (how to calculate distance)            
    * find path (go out)
        > take out current location  
        > check if it reaches the end  
        > * if reaches the end  
              1. create a path;  
              2. before goes back the the start point  
                - push current location into path;  
                - take out pre location from table
                - color marker  
                - repeat above until goes back to the start  
        > * if not  
              1. insert the next point
2. Sorted class
    * give 
        > go in: push in
    * take
        > go out: 
            1. edge cases: empty  
            2. initial the min value and index as [0] && 0 (also use to store the value)    
            3. start from index 1, compare and replace min and minIndex  
            4. delete current min:  
                - switch with current last index value;  
                - pop()  
                  * in this way, it's O(1), only change one time;
3. optional color marker of best way
