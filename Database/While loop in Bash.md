202206131508
Tags: #bash_script

---

# While loop in Bash

```bash
# Loop through all the positional parameters

while [[ "${#}" -gt 0 ]]
do
  echo "Number of parameters: ${#}"
  echo "Parame ter 1: ${1}"
  echo "Parameter 2: ${2}"
  echo "Parameter 3: ${3}"
  echo
  shift
done
```

---
## Links