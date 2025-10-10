# MY_NOTES

Getting Ram usage per user in sorted order
ps -eo user,rss | awk '{sum[$1]+=$2} END {for (u in sum) printf "%-15s %.2f GB\n", u, sum[u]/1024/1024}' | sort -k2 -nr
