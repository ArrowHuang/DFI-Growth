# DFI-Growth

**–*What is DFI-Growth?***     
  DFI-Growth is an algorithm for deriving frequent itemsets from frequent closed itemsets by pattern growth.

**–*What is the input of the DFI-Growth algorithm?***    
  The input of DFI-Growth is a FCI database.
  A FCI database is a set of frequent closed itemsets.    
  For example, consider the following FCI database. It contains 6 frequent closed itemsets and support number of each itemset. This database is provided as the file **contextMushroom_FCI90.txt**.  
  This input file was obtained by applying the Charm algorithm (proposed by Zaki) on the Mushroom.txt dataset with 90% as the minsup threshold.    
  
  | frequent closed itemsets      | support     | 
  | ---------- | :-----------:  | 
  | {36  90  97}    | 	7576     | 
  | {90  97}        |   7768     | 
  | {36  90  94}    |   8192     | 
  | {36  90}        |   8200     | 
  | {90  94}        |   8216     | 
  | {90}            |   8416     |   
  
**–*What is the output of the DFI-Growth algorithm?***    
  DFI-Growth is an algorithm for deriving frequent itemsets from frequent closed itemsets.   
  A frequent itemset is an itemset which appears in at least minsup transactions from the transaction database. And a frequent closed itemset is a frequent itemset that none of its immediate supersets have the same support number as itself. 
  For example, if DFI-Growth is run on the previous FCI database,  DFI-Growth produces the following result:   
  
   | frequent closed itemsets      | support     | 
  | ---------- | :-----------:  | 
  | {36  97}        | 	7576     | 
  | {36  90  97}    |   7576     | 
  | {90  97}        |   7768     | 
  | {97}            |   7768     | 
  | {36  94}        |   8192     | 
  | {36  90  94}    |   8192     | 
  | {90  94}        | 	8216     | 
  | {94}            |   8216     | 
  | {36}            |   8200     | 
  | {36  90}        |   8200     | 
  | {90}            |   8416     | 
  
  
  More details about DFI-Growth please refer to [SPMF](http://www.philippe-fournier-viger.com/spmf/ "悬停显示")
