# utl-python-base64-encode-and-decode-a-binary-execl-workbook-or-binary-file
Python base64 encode and decode a binary execl workbook or binaryfile
    Python base64 encode and decode a binary execl workbook

        Steps in Python code

            1. Read entire binary file into Python string object (can be as large as memory?)
            2. base 64 encode binary file into clear ascii (A-Z a-z + /)
            3. Decode the binary file created into Python string object (can be as large as memory?)
            4. Decode and open decoded excel workbook to check process

         'pybase64' package may be faster?
          There are options for safe encode/decode for "utf#" and "url", passwords?

    Maybe this is best done by Python?

    github
    https://tinyurl.com/y5d2j6z2
    https://github.com/rogerjdeangelis/utl-python-base64-encode-and-decode-a-binary-execl-workbook-or-binary-fil

    *_                   _
    (_)_ __  _ __  _   _| |_
    | | '_ \| '_ \| | | | __|
    | | | | | |_) | |_| | |_
    |_|_| |_| .__/ \__,_|\__|
            |_|
    ;

    * Make binary excel workbook;

    libname xel "d:/xls/class.xlsx";
    data xel.class;
      set sashelp.class;
    run;quit;
    libname xel clear;

    Here is what a excel workbook looks like in binary

    d:/xls/class.xlsx
    =================

    *                                        _    _                 _
     _ __ __ ___      __ __      _____  _ __| | _| |__   ___   ___ | | __
    | '__/ _` \ \ /\ / / \ \ /\ / / _ \| '__| |/ / '_ \ / _ \ / _ \| |/ /
    | | | (_| |\ V  V /   \ V  V / (_) | |  |   <| |_) | (_) | (_) |   <
    |_|  \__,_| \_/\_/     \_/\_/ \___/|_|  |_|\_\_.__/ \___/ \___/|_|\_\

    ;

    * unprintable bytes may not align with ruler, because of tabs/CR...

    --- RECORD NUMBER ---  1   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    PK.....!.œ×ü¨^..<...Ï[Content_Types].xml ¢Ë( ............................................
    540010000000209DFA5000300010C054667667557767527662AC02A000000000000000000000000000000000000000000000
    0B344060800010C7C8E100C40030F1B3FE45E4F49053DE8DC02B180020000000000000000000000000000000000000000000

     --- RECORD NUMBER ---  2   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    ....................................................................................................
    0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
    0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
    ....
    ....
     --- RECORD NUMBER ---  6   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    .......¬“ËNÃ0E÷HüCä-JÜ²@5í‚Çº(`ìIcÕ/yÜ6ý{Æ      ­*UÙÄŠ¬¹wæÌõdÖYSl ¢ö®fãjÄ
pÒ+í–5{_¼”÷¬À$œÆ;¨Ù
    000000000000A9C4C314F4F4E24DB403E8C1B216E46D27D3F7C0A0215DC8AB7ECF6D5562AFA6E6C07D2E9375B9FAC291C3AD
    000000000000C3BE300578C34DAC2085D272A8F0C935F9C6DB69D4A5594AC976C54693C026E63A4A02BD65BFC47C04C26B89


     --- RECORD NUMBER ---  7   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    Í¦×W“Å..Tí°fmJás”-X•àè¦ñÑŠD¿qÉƒ+±~;Ýqé]—Ê”5ØtòF ­ ˜‹˜^…%ÞžH   ï¸"=V<…Ù»f"£¥HÔ9ß8õÃµôM£
    09CAD59C2015EB664E87925890EEAFD84B7C892B0731D7E509C93D7F404AA9895821D19408EB235308DB620AA4D3D3FCBF4A
    E0D67735E064D06DA1134D815F08611A4F1930B14EBAD19D27A458426D4D08B8E55FE9E8D6F82D6CE59B62435849F85354D3


     --- RECORD NUMBER ---  8   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    %(/×–¼ª^ì&«ð_    íàÅV"…-@²¦D÷ÎOÐˆµIÅsGèž7ÚÌŠ*ûñ±ÕO8lmóÃ@Û¼Œ®Ì7ÄãHW§yŸæ¸õqõáýê¿If¢•Úíg=Úø<
    222D9BA5E2AF503E0EC5120824BA14FC4D8B4C7400E1093D1C82FFBD04366FC4DB8AC3CE45A79EBF7FEFEB46A91DE6311DF3
    58F76CAEC6B0FD1DC0568285D026A47EF08595374681CE7A7CAAB1151F8CD330BCCEC7438779F685151DAF96255AD7D6CA8C


     --- RECORD NUMBER ---  9   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    ú€œòqq×¤@•$!&    ÎÇ¼)´yö~õÈûãòä~ÓAÿO¤p>„}¾rõ‘Éyÿö§Ÿ...ÿÿ.PK.....!.äù%S..Ü...½_rels/.r
    F89F7709DA49822200CCB2B7F7FCFEFE78D4F40A87387B7F9C7FFA9000FF0054001000000020EF250000D00000B057667227
    A0C2113074051416D7E7C9496E58B324EF31FFC4F0E4DE25199F67F000FF300B34406080001049536100C200B0D1F25C3FE2

    *                         _          _
      ___ _ __   ___ ___   __| | ___  __| |
     / _ \ '_ \ / __/ _ \ / _` |/ _ \/ _` |
    |  __/ | | | (_| (_) | (_| |  __/ (_| |
     \___|_| |_|\___\___/ \__,_|\___|\__,_|

                        _    _                 _
    __      _____  _ __| | _| |__   ___   ___ | | __
    \ \ /\ / / _ \| '__| |/ / '_ \ / _ \ / _ \| |/ /
     \ V  V / (_) | |  |   <| |_) | (_) | (_) |   <
      \_/\_/ \___/|_|  |_|\_\_.__/ \___/ \___/|_|\_\

    ;

    Note clear ascii text (a-z, A-Z, / and +) replaces unprintable chars
    Hex ruler does line up because 'bad' bytes do not exist;


     --- RECORD NUMBER ---  1   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    UEsDBBQABgAIAAAAIQCc1/yoXgEAADwEAAATAM8BW0NvbnRlbnRfVHlwZXNdLnhtbCCiywEooAACAAAAAAAAAAAAAAAAAAAAAAAA
    5474445446444444454632765644447444454434534766566656546755464667644677466444444444444444444444444444
    553422112719111191331F9F8751147511141D8270E62E2C2E2668C7A8E4CE842339975FF113111111111111111111111111


     --- RECORD NUMBER ---  2   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
    4444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444
    1111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111
    ....
    ....
    ....

     --- RECORD NUMBER ---  6   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
    4444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444
    1111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111


     --- RECORD NUMBER ---  7   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACsk8tOwzAQRfdI/EPk
    4444444444444444444444444444444444444444444444444444444444444444444444444444444444476374774556642456
    111111111111111111111111111111111111111111111111111111111111111111111111111111111133B84F7A112649F50B


     --- RECORD NUMBER ---  8   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    LUrcskAINe2CxxK6KB9g7Elj1S953Db9e8YJrQQqFVXZxIqsuXfmzPVk1llTbCCi9q5m42rECnDSK+2WNXtfvJT3rMAknBLGO6jZ
    4576764446347743443634663533346363547557455574777566755636656446373633744645423545767453744664444365
    C5233B19E52388B6B29775CA13953429589A2111668A8913586DA06B1CC42339915D42253E43BB27E8466A432D1BE2C7F6AA


     --- RECORD NUMBER ---  9   ---  RECORD LENGTH ----   100

    1...5....10...15...20...25...30...35...40...45...50...55...60...65...70...75...80...85...90...95...
    DpDNptdXk8UuABZU7bBmbUrhgXOULViBlQ/g6Kbx0YpEv3HJg5ArsQR+OxrdceldApfKlDXYdPJGDUStoJiLmF6FJR/eGZ5IDYbv
    4744776563574455364665766545456465263467357473446347755247766666476464556544455764646434452645344567
    404E0448B85512A5722D252878F5C692C1F76B280905638A7512312BF82435C4106BC48940A74534FA9CD666A2F57A594926

    *          _       _   _
     ___  ___ | |_   _| |_(_) ___  _ __
    / __|/ _ \| | | | | __| |/ _ \| '_ \
    \__ \ (_) | | |_| | |_| | (_) | | | |
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|

    ;

    %utl_submit_py64('
    import base64;
    data = open("d:/xls/class.xlsx", "rb").read();
    encoded = base64.b64encode(data);
    with open("d:/txt/class_encode.txt", "wb") as f:;
    .    f.write(encoded);
    with open("d:/txt/class_encode.txt", "rb") as g:;
    .    b64encode_from_file=g.read();
    decoded=base64.b64decode(b64encode_from_file);
    with open("d:/xls/class_decode.xlsx", "wb") as w:;
    .    w.write(decoded);
    ');

