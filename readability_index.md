#!/bin/python3

import math
import os
import random
import re
import sys



def automated_readability_index(sentence):
    letters = len(sentence)-sentence.count(" ")
    words = len(sentence.split())
    result = (4.71 * (letters/words) + 0.5 * (words/1) - 21.43)
    rounded = math.ceil(result)
    return 14 if rounded > 14 else rounded 
   

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    sentence = input()

    output = automated_readability_index(sentence)

    fptr.write(str(output) + '\n')

    fptr.close()
    

    
  

