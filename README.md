# DataFlow
GCP DataFlow

#Windows #Stream
so far we used to finate data for analyze  segregate and aggregate
storage system
database till now

but for straming data
2 min window

keep and agreegate

Window Time Notion

event time(actual user rating time)(late element latency)
processing Time(the time our system recieved)(Latency)


#Tumbling/Sliding Window


#Tumbling
    134        732         35
2:12   2:08        2:04         2:00
     s=8       s=12       s=8
#Sliding Window
Window = 4min
Sliding Interval -> 2mins

    134        732         35
2:12   2:08        2:04         2:00
     
                    <-----Window2--->
           2:06<--Window2--->2:02
     2:08<-W3->2:04

Rating.csv -> Publisher  Ratings ---> Processor  RatingCounts----> Subscriber

process fixed window 10 seconds, total nof ratings recieved
for each movie in 10 sec window

#SessionWindow

same session for specific drama gener
it will creeate session and append to same session if
data won't come the session will close.

session is used to check the continuouse data time

#LateElement
             <--window1-->    <--window2-->
10:03     |  10:06  10:07  |  10:04  10:02
 10       |    2      7    |    3      5
        10:15            10:10             10:05


while processing the system time based we get the data but actual entery time data some time comes late to the system for that we introduce one more parameter


