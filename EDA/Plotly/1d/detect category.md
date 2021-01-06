link [stackoverflow ](https://stackoverflow.com/questions/35826912/what-is-a-good-heuristic-to-detect-if-a-column-in-a-pandas-dataframe-is-categori)
count unique
count total 
ratio = unique/total 
Set [[category_threshold]] to ratio. 
Set max count. 
	count < 100, threshold 0.2 
	count > 100, threshold 0.1 
Set max unique.
	false if unique > 20 

