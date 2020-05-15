##Script # 1##
# Zoom-chat-most-active

# Purpose: Figure out who is most active in the zoom chat logs. 

# Step 1 : Save the chat log via zoom : https://support.zoom.us/hc/en-us/articles/115004792763-Saving-in-meeting-chat

# Step 2 : Open terminal on your machine : https://www.google.com/search?q=open+terminal
# Note : If you are using windows, then you may have to use cygwin. 

# Step 3 : type or paste the following command on your terminal (below): 

cat meeting_saved_chat.txt | awk '{ print $3" "$4}' |sort -n | uniq -c |sort

# Note : Where 'meeting_saved_chat.txt' is the name of the actual text file that contains the chatlog. 

# Your output will look something like this. 

   5 Tori Amos
   
   5 Olie Kramern
 
   11 David Hillier 
   
   13 Keith Urban 
   
   16 William La 
   
   24 Ab Lincoln 
   
   38 Fraser Jaleel

Note: If you get private messages and/or reply back to private messages, then the you need to consider that in the count. 

##Script # 2##
# Extracting URLs#
Note: This script may not work 100%. Because, URLs typed like this may not be scraped by this script --> cnn.com 

# Follow step 1 and 2 above. 

# Step 3: type or paste the following command on your terminal (below):

cat meeting_saved_chat.txt | grep -i "www \| http"
# Note : Same note as in Script # 1 (above)
