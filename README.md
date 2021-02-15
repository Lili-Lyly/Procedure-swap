# Procedure-swap

PROCEDURE swap(VAR xp, VAR yp : INTEGER)
VAR
   tmp : INTEGER;
BEGIN
  tmp := xp;
  xp := yp;
  yp := tmp;
END
/* *** Bubble sort *** */
PROCEDURE bubble_sort(VAR tab : ARRAY_OF INTEGER)
VAR
   i,j,n : INTEGER;
BEGIN
   n := tab.length;
   FOR i FROM 0 TO n-2 STEP 1  DO
       // Last i elements are already in place
       FOR j  FROM 0  TO n-i-2 STEP 1  DO
           IF (tab[j]>tab[j+1]) THEN
               swap(tab[j], tab[j+1])
           END_IF
       END_FOR
   END_FOR
END
