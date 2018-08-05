# Understanding Java Garbage Collection and what you can do about it

## Source

   - https://www.youtube.com/watch?v=we_enrM7TSY  
   - http://www.entpnerd.com/2018/08/05/notes-from-gil-tenes-talk-understanding-java-garbage-collection-and-what-you-can-do-about-it/
   - https://www.cubrid.org/blog/understanding-java-garbage-collection/
   - https://www.cubrid.org/blog/how-to-monitor-java-garbage-collection/
   - https://www.cubrid.org/blog/how-to-tune-java-garbage-collection/
   - https://docs.oracle.com/javase/8/docs/technotes/guides/vm/gctuning/index.html
   - https://www.oracle.com/technetwork/articles/java/g1gc-1984535.html
   - https://dzone.com/articles/g1gcgarbage-first-garbage-collector-tuning-flags-1
   - https://aikar.co/2018/07/02/tuning-the-jvm-g1gc-garbage-collector-flags-for-minecraft/
   - https://developer.amd.com/4-easy-ways-to-do-java-garbage-collection-tuning/
   
## Quotes

   - "Many a little makes a mickle."

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

