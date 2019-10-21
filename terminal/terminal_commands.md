# Terminal

## Find the largest file
sudo find / -type f -printf '%s %p\n' | sort -nr | head -10
