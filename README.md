##Leetcode Weekly Contest 195
###1496. Path Crossing

    ```
    class Solution {
        public boolean isPathCrossing(String path) {
            char[] array = path.toCharArray();
            int x = 0, y = 0 ;
            HashSet<String> set = new HashSet<String>();
            String temp = "";
            set.add("00");
            for(char c : array)
            {
                if(c == 'N')
                {
                    y +=1;
                }
                if(c == 'S')
                {
                    y -=1;
                }
                if(c == 'E')
                {
                    x +=1;
                }
                if(c == 'W')
                {
                    x -=1;
                }
                temp = String.valueOf(x)+String.valueOf(y);
                if(!set.add(temp))
                {
                    return true;
                }
            }
            return false;
        }
    }
    ```
