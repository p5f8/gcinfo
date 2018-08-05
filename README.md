# Understanding Java Garbage Collection and what you can do about it

## Source

https://www.youtube.com/watch?v=we_enrM7TSY  

## Mechanisms of GC

### Copy
   
   - Requires 2x times the memory space.  

### Mark/Compact

   - Requires 2x times the memory space.  
   
### Mark/Sweep/Compact
   
   - Requires 1.3x times the memory space.  
   
### Generational Collection
  
   - Weak Generational Hypothesis: "most objects die young"  
   - Focus on young generation  
   - Only collect older generations  
   - Requires a "Remembered set": track all references into the young generation from the outside.   
   - Immediate promotion can significantly reduce gen. filter efficiency  
   - Waiting too long to promote can eliminate generational benefits  
   - Usually keep surviving objects in young generation for a while before promoting them to the old generation.  
   - 

## Paused at 51:54

