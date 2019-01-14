# r_assignment_wk3
#
# create cached inverted matrix
#
makeCacheMatrix <- function(x = numeric()) {
# set initial values
+         m <- NULL
+                 x <<- y
+                 m <<- NULL
+         }
# invert matrix and save result in m
+         get <- function() x
+         setslv <- function(solve) m <<- solve
+         getslv <- function() m
+         list(set = set, get = get,
+              setslv = setslv,
+              getslv = getslv)
+ }
###
# invert matrix unless already done
> cacheSolve <- function(x, ...) {
# if m already exists, use cached data
+         m <- x$getslv()
+         if(!is.null(m)) {
+                 message("getting cached data")
+                 return(m)
+         }
# if m does not exist, use solve function on matrix
+         data <- x$get()
+         m <- solve(data, ...)
+         x$setslv(m)
+         m
+ }
###
