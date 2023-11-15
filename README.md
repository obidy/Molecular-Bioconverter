#def mm_to_um(mm):
  return mm * 1000

def mm_to_nm(mm):
  return mm * 1000000

def mm_to_micron(mm):
  return mm

def um_to_mm(um):
  return um / 1000

def um_to_nm(um):
  return um * 1000

def um_to_micron(um):
  return um / 1000

def nm_to_mm(nm):
  return nm / 1000000

def nm_to_um(nm):
  return nm / 1000

def nm_to_micron(nm):
  return nm / 1000000

def micron_to_mm(micron):
  return micron

def micron_to_um(micron):
  return micron * 1000

def micron_to_nm(micron):
  return micron * 1000000

def convert_length():
  value = float(input("Enter the measurement value: "))
  from_unit = input("Enter the current unit (mm, um, nm, micron): ")
  to_unit = input("Enter the target unit (mm, um, nm, micron): ")

  result = 0

  if from_unit == "mm":
      if to_unit == "um":
          result = mm_to_um(value)
      elif to_unit == "nm":
          result = mm_to_nm(value)
      elif to_unit == "micron":
          result = mm_to_micron(value)
      else:
          print("Invalid target unit.")
          return
  elif from_unit == "um":
      if to_unit == "mm":
          result = um_to_mm(value)
      elif to_unit == "nm":
          result = um_to_nm(value)
      elif to_unit == "micron":
          result = um_to_micron(value)
      else:
          print("Invalid target unit.")
          return
  elif from_unit == "nm":
      if to_unit == "mm":
          result = nm_to_mm(value)
      elif to_unit == "um":
          result = nm_to_um(value)
      elif to_unit == "micron":
          result = nm_to_micron(value)
      else:
          print("Invalid target unit.")
          return
  elif from_unit == "micron":
      if to_unit == "mm":
          result = micron_to_mm(value)
      elif to_unit == "um":
          result = micron_to_um(value)
      elif to_unit == "nm":
          result = micron_to_nm(value)
      else:
          print("Invalid target unit.")
          return
  else:
      print("Invalid current unit.")
      return

  print(f"{value} {from_unit} is equal to {result} {to_unit}.")

# Main function for testing
def main():
  convert_length()

if __name__ == "__main__":
  main()
