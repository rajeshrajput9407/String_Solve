# String_Solve
string solve problem

first,first>Second,first>Second>Third,first>Second>Third>Four,first>Second>Third>Four>Five

    static void Main(string[] args)
        {
            string[] my = new string[] {
                "first",
                "Second",
                "Third",
                "Four",
                "Five"
            };
            string mystring = string.Empty;
           
            for (int i = 0; i < my.Length; i++)
            {
                string temp = string.Empty;
                if (mystring==string.Empty)
                {
                    mystring = my[i] + ",";
                }
                if (i>0)
                {
                    for (int j = 0; j < i + 1; j++)
                    {
                        temp = temp + my[j] + ">";
                    }
                    temp= temp.Remove(temp.Length - 1, 1) + ",";
                    mystring = mystring + temp;
                }
               
            }
        }


Output:
first,first>Second,first>Second>Third,first>Second>Third>Four,first>Second>Third>Four>Five
