/*********************************************************************************
/*Name        :Two-Sum
/*Author      :YY
/*Version     :1.0_Harsh_Twice
/*Copyright   :
/*Description :O(n) O(n)
/*********************************************************************************
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        map<int,int> harsh_map;        //建立hash表存放数组元素
     	vector<int> vec(2,-1);         //初始化为？存放结果
     	for(int i=0;i<nums.size();i++)
            harsh_map.insert(map<int,int>::value_type(nums[i],i));
            for(int i=0;i<nums.size();i++){
                if(harsh_map.count(target-nums[i])>0&&(harsh_map[target-nums[i]]!=i))
      	        //判断是否找到目标元素且目标元素不能是本身
      	      {
     	           vec[0]=i;
     	           vec[1]=harsh_map[target-nums[i]];
     	           break;
       	     }
      	  }
     	   return vec;
   	 }
}

