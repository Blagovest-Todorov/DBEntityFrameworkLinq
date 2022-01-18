# DBEntityFrameworkLinq
examplesEFLinq


using System;
using System.Collections.Generic;
using System.Linq;

namespace LinqDemo
{
    class Program
        {
        /// go to DB table songs select only songs starting with H and give me the count /Linq is used to retrieve Info from DB here in this case :
        static void Main(string[] args)
        {
            var db = new MusicContext();
            var songs = db.Songs.Where(x => x.StartsWith("H")).toList();
            Console.WriteLine(db.songs.Count());
            
        }
    }    
}
