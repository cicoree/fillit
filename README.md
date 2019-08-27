# Fillit

## Function Flow
In main.c: 
1. **read** is called with argument *argv[1]*

In read.c  

2. **read** calls on **open** to get the input from *argv[1]* (the filename)
3. **read** creates a 546 character string called *buffer* which stores the input  
4. **read** returns **makelist** (to make the piecelist out of the buffer)  
5. **makelist** calls on **makepiece** to slice the buffer into max 26 pieces (nodes of type t_piece)  
6. **makepiece** calls on **align** and returns each *piece* aligned (?)  

In shift.c

7. **align** calls on **shift_x** and **shift_y** to move *piece* one up and one left in case none of its x or y coords are zero (?)  

Back in read.c

8. **makelist** returns a pointer to the first piece (*beginning*) of the *piecelist*  

Back in main.c  

9. **solve** is called with argument *piecelist*
