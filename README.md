<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <title>Doa Sehari-hari</title>
    <style>
        body {background-color: powderblue;}
        p {
            border-style: solid;
            border-width: medium;
            border-color: black;
            }
    </style>
</head>
<body>
               
    <div class="container mt-5">
        <h1>Doa Sehari-hari</h1>
            <input id="search_input" type="text" placeholder="Search...">   
            <button onclick="searchPosts(0)">Search</button>   
               
            <div id="search results"></div> 
        <div id="output"></div>

        <script type="text/javascript">
            var data = {
                "doa_doa": [
                    {
                        "no":"1",
                        "doa":"Doa ketika turun hujan",
                        "ayat":"اللَّهُمَّ صَيِّبًا نَافِعًا",
                        "latin":"Allahumma shayyiban nafi’an.",
                        "artinya":"Ya Allah, curahkanlah air hujan yang bermanfaat. (HR Bukhar dari Aisyah RA)"
                    },
                    {
                        "no":"2",
                        "doa":"Doa ketika takut bahaya hujan lebat",
                        "ayat":"اللَّهُمَّ حَوَالَيْنَا وَلاَ عَلَيْنَا ، اللَّهُمَّ عَلَى الآكَامِ وَالظِّرَابِ ، وَبُطُونِ الأَوْدِيَةِ ، وَمَنَابِتِ الشَّجَرِ",
                        "latin":"Allahumma hawalaina wala ‘alaina. Allahumma ‘alal akami wa adhirabi, wa buthunil auwdiyati, wamanabitisyajari.",
                        "artinya":"Ya Allah turunkan hujan ini di sekitar kami jangan di atas kami. Ya Allah curahkanlah hujan ini di atas bukit-bukit, di hutan-hutan lebat, di gunung-gunung kecil, di lembah-lembah, dan tempat-tempat tumbuhnya pepohonan. (HR Bukhari Muslim)"
                    },
                    {
                        "no":"3",
                        "doa":"Doa setelah turun hujan",
                        "ayat":"مُطِرْنَا بِفَضْلِ اللـهِ ورَحْمَتِهِ",
                        "latin":"Muthirnaa bifadhlillahi wa rahmatihi.",
                        "artinya":"Diturunkan kepada kami hujan berkat anugerah Allah dan rahmat-Nya. (HR Bukhari)"
                    },
                    {
                        "no":"4",
                        "doa":"Doa bertemu binatang buas",
                        "ayat":"إِنَّهُۥ مِن سُلَيْمَٰنَ وَإِنَّهُۥ بِسْمِ ٱللَّهِ ٱلرَّحْمَٰنِ ٱلرَّحِيمِ",
                        "latin":"Innahụ min sulaimāna wa innahụ bismillāhir-raḥmānir-raḥīm",
                        "artinya":"Sesungguhnya surat itu, dari SuIaiman dan sesungguhnya (isi)nya: Dengan menyebut nama Allah Yang Maha Pemurah lagi Maha Penyayang. (Qs. An Naml: 30 )"
                    },
                    {
                        "no":"5",
                        "doa":"Doa agar selalu dicukupkan rezeki",
                        "ayat":"اَللّٰهُمَّ اَكْفِنِيْ بِحَلَالِكَ عَنْ حَرَامِكَ، وَأَغْنِنِيْ بِفَضْلِكَ عَمَّنْ سِوَاكَ",
                        "latin":"Allahummakfini bihalalika ‘an haramik wa aghnini bifadhlika amman siwak",
                        "artinya":"Ya Allah, berilah aku kecukupan dengan rezeki yang halal, sehingga aku tidak memerlukan yang haram, dan berilah aku kekayaan dengan karuniamu, sehingga aku tidak memerlukan bantuan orang lain, selain diri-mu. (HR. Ahmad)"
                    },
                    {
                        "no":"6",
                        "doa":"Doa ketika menyisir rambut",
                        "ayat":"اَللّهُمَّ حَرِّمْ شَعْرِى وَبَشَرِى عَلىَ النَّار",
                        "latin":"ALLAHUMMA HARRIM SYA'RII WA BASYARII 'ALAN NAAR",
                        "artinya":"Ya Allah, halangilah rambut dan kulitku dari api neraka"
                    },
                    {
                        "no":"7",
                        "doa":"Doa memohon ilmu yang bermanfaat",
                        "ayat":"اَللّٰهُمَّ اِنِّى اَسْأَلُكَ عِلْمًا نَافِعًا وَرِزْقًا طَيِّبًا وَعَمَلاً مُتَقَبَّلاً",
                        "latin":"Allahumma innii as-aluka 'ilmaan naafi'aan wa rizqoon thoyyibaan wa 'amalaan mutaqobbalaan",
                        "artinya":"Ya Allah, sesungguhnya aku mohon kepada-Mu ilmu yang berguna, rezki yang baik dan amal yang baik Diterima. (H.R. Ibnu Majah)"
                    },
                    {
                        "no":"8",
                        "doa":"Doa sebelum belajar",
                        "ayat":"يَارَبِّ زِدْنِىْ عِلْمًا وَارْزُقْنِىْ فَهْمًا",
                        "latin":"Yaa robbi zidnii 'ilman warzuqnii fahmaa",
                        "artinya":"Ya Allah, tambahkanlah aku ilmu dan berikanlah aku rizqi akan kepahaman"
                    },
                    {
                        "no":"9",
                        "doa":"Doa sesudah belajar",
                        "ayat":"اَللّٰهُمَّ اِنِّى اِسْتَوْدِعُكَ مَاعَلَّمْتَنِيْهِ فَارْدُدْهُ اِلَىَّ عِنْدَ حَاجَتِىْ وَلاَ تَنْسَنِيْهِ يَارَبَّ الْعَالَمِيْنَ",
                        "latin":"Allaahumma innii astaudi'uka maa 'allamtaniihi fardud-hu ilayya 'inda haajatii wa laa tansaniihi yaa robbal 'alamiin",
                        "artinya":"Ya Allah, sesungguhnya aku menitipkan kepada Engkau ilmu-ilmu yang telah Engkau ajarkan kepadaku, dan kembalikanlah kepadaku sewaktu aku butuh kembali dan janganlah Engkau lupakan aku kepada ilmu itu wahai Tuhan seru sekalian alam."
                    }
                ]
            };

            var doaDoaList = data.doa_doa;
            var output = document.getElementById('output');

            function searchPosts( loadedResults ){  
      
                var query = document.getElementById( "search_input" ).value;  
                var resultsContainer = document.getElementById( "search_results" );  
                    
                if( loadedResults === 0 ){  
                    resultsContainer.innerHTML = "";  
                }  

                var xmlhttp = new XMLHttpRequest();  
    
                xmlhttp.onreadystatechange = function() {  
                    if ( xmlhttp.readyState === 4 && xmlhttp.status === 200 ) {  
                        // fetch response text   
                        var response=xmlhttp.responseText;  
                        var outputPosts;   
                     
                        try{  
                            outputPosts = JSON.parse( response );  
                        }  
                        catch( e ){  
                            return;  
                        }  
        
                        for( var i = 0; i < outputPosts.length; i++ ){  
                            // append result to result container, link to url of post  
                            resultsContainer.innerHTML += "<div id='result_" + i + "'><a href='http://" + outputPosts[ i ].url + "'><h3>" + outputPosts[ i ].title + "</h3>" + outputPosts[ i ].description + "</a><div>";  
                        }  
                        // add button to load more results starting from the last loaded result (remove any existing button first if one exists)  
                        try{  
                            document.getElementById( "load_button" ).remove();  
                        }  
                        catch( e ){  
                            return;  
                        }  
                        finally{  
                            resultsContainer.innerHTML += "<br><button id='load_button' onclick='searchPosts( " + ( loadedResults + outputPosts.length ) + " )'>Load more</button>";  
                        }  
                    }  
                };  
                    
                // send request to fetch searchDB.php  
                xmlhttp.open( "GET", "searchDB.php?search=" + query + "&loaded=" + loadedResults, true );  
                xmlhttp.send();  
            }

            function displayDoaDoa() {
                var html = '<table class="table table-bordered"><thead><tr><th>No</th><th>Doa</th><th>Ayat</th><th>Latin</th><th>Artinya</th></tr></thead><tbody>';
                doaDoaList.forEach(function(doa) {
                    html += '<tr><td>' + doa.no + '</td><td>' + doa.doa + '</td><td>' + doa.ayat + '</td><td>' + doa.latin + '</td><td>' + doa.artinya + '</td></tr>';
                });
                html += '</tbody></table>';
                output.innerHTML = html;
            }

            // Memanggil fungsi untuk menampilkan data doa-doa
            displayDoaDoa();

        </script>

        <script src="https://cdn.jsdelivr.net/npm/bootstrap@">
        </script>

        <script src="./script.js">
        </script>
    
</body>    
