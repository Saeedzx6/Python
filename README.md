# functhion to check if th ip address is valid or not
import pandas as pd
def validate_ip(ip):
    octets = ip.split('.')   
    # Check for valid IPv4 address format and ensure each octet is within range [0, 255] without leading zeros
    if len(octets) != 4:
        return False
      for octet in octets:
          if not octet.isdigit() or not (0 <= int(octet) <= 255) or (len(octet) > 1 and octet[0] == '0'):
              return False
     return True
