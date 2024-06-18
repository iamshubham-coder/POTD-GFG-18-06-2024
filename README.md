# POTD-GFG-18-06-2024
No. of rectangle in a circle
THE PROBLEM CAN BE THOUGHT AS TRYING TO FIT A RECTANGLE OF CERTAIN SIZEEITH IN A CIRCLE 
BASIC APPROACH

1)Calculate the bounding box: The maximum width and height of the rectangle that can fit inside the circle will be  
2R, which is the diameter of the circle.

2)Iterate through possible positions: You need to check each possible position where the bottom-left corner of the rectangle can be placed such that the entire rectangle stays within the circle.

3)Check if the rectangle fits: For each position, check if all corners of the rectangle lie within the circle.
CODE OF THIS PROBLEM IS ATTACHED IN THE TEXT FILE 


class Solution {
  public:
    int rectanglesInCircle(int r) {
        int count=0, max=2*r;
        
        for(int i=1; i<=max; ++i)
        
        {
            for(int j=1; j<=max; ++j)
            {
                if(i*i+j*j <= 4*r*r)
                    count++;
            }
        }
        return count;
     }
     };
