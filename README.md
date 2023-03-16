# python
# Gates in python 


  class SRFlipFlop:
    def _init_(self):
        self.Q = 0
        self.Qbar = 1
        
    def set_inputs(self, S, R):
        if S == 1 and R == 0:
            self.Q = 1
            self.Qbar = 0
        elif S == 0 and R == 1:
            self.Q = 0
            self.Qbar = 1
        elif S == 1 and R == 1:
            self.Q = self.Q
            self.Qbar = self.Qbar
        elif S == 0 and R == 0:
            self.Q = self.Q
            self.Qbar = self.Qbar
            
    def get_outputs(self):
        return self.Q, self.Qbar
    
flipflop = SRFlipFlop()

flipflop.set_inputs(1, 0)
print(flipflop.get_outputs()) # Output: (1, 0)

flipflop.set_inputs(0, 1)
print(flipflop.get_outputs()) # Output: (0, 1)

flipflop.set_inputs(1, 1)
print(flipflop.get_outputs()) # Output: (0, 0)

flipflop.set_inputs(0, 0)
print(flipflop.get_outputs()) # Output: (0, 1)
