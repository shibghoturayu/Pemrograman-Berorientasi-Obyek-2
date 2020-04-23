# Pemrograman-Berorientasi-Obyek-2
Source Code C# Retail Item Class

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace UTSPBONOMER2
{
        public class RetailItem
        {
            private String description;
            private int unitsOnHand;
            private double price;

            public void setDescription(String userDescription)
            {
                description = userDescription;
            }

            public void setUnitsOnHand(int userUnitsOnHand)
            {
                unitsOnHand = userUnitsOnHand;
            }

            public void setPrice(double userPrice)
            {
                price = userPrice;
            }

            public String getDescription()
            {
                return description;
            }
            public int getUnitsOnHand()
            {
                return unitsOnHand;
            }

            public Double getPrice()
            {
                return price;
            }

            public RetailItem(String descriptionGiven, int unitsOnHandGiven, double priceGiven)
            {
                description = descriptionGiven;
                unitsOnHand = unitsOnHandGiven;
                price = priceGiven;
            }
        }
    
}



using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace UTSPBONOMER2
{
    class Program
    {
        static void Main(string[] args)
        {
            RetailItem[] item = new RetailItem[3];

            item[0] = new RetailItem("Jacket", 12, 59.95);
            item[1] = new RetailItem("Jeans", 40, 34.95);
            item[2] = new RetailItem("Shirt", 20, 24.95);

            Console.WriteLine("=============================================");
            Console.WriteLine("\tDescription\tUnits On Hand\tPrice");
            Console.WriteLine("=============================================");
            for (int i = 0; i < item.Length; i++)
            {
                Console.WriteLine("Item " + (i + 1) + "\t" + item[i].getDescription() + "\t\t" + item[i].getUnitsOnHand() + "\t\t" + item[i].getPrice());
            }
            Console.WriteLine("=============================================");
            Console.ReadKey();
        }
    }
}

