# DBEntityFrameworkLinq
examplesEFLinq


using System;
using System.Collections.Generic;
using System.Linq;

namespace LinqDemo
{
    class Program
    {
        static void Main(string[] args)
        {
            var db = new MusicContext();
            var songs = db.Songs.Where(x => x.StartsWith("H")).toList();
            Console.WriteLine(db.Songs.Count());
            
        }
    }    
}
