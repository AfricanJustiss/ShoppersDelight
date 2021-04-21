The code for this program is below. I provide a quick explanation on what the code is trying to convey afterwards.

       
       extension Array {
       var combinations: [[Element]] { 
       if count == 0 { [self]
        }
        else {
          
          let tail = Array(self[1..<endIndex])
            let head = self[0]

            let first = tail.combinations
            let rest = first.map { $0 + [head] }

            return first + rest
        }
    }
    }
    print([1,2,2,2,3,3,4].combinations)






//  The shoppers delight program is meant to find all possible combinations of purchases given a set of options. For example, a lunch menu.  In order to do that, i had to establish in swift thhat i was looking for combinations, what to bring back, and how to present it. Once that was complete, all i had left to do was to establish what i needed to be printed, which of course would be the sequence. To make things easier to read, i chose numbers instead of food items. Once i added that sequence in, and establised my combination rule, viola! We have all the purchase possibilities.
