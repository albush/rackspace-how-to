---
permalink: define-mime-types-on-your-windowsiis-based-site/
node_id: 558
title: Define mime types on your Windows/IIS based site
type: article
created_date: '2011-03-16'
created_by: Rackspace Support
last_modified_date: '2015-06-12'
last_modified_by: Kelly Holcomb
product: Cloud Sites
product_url: cloud-sites
---

To add an additional extension or change the mime type for an extension,
use the following code:

    <configuration>
    <system.webServer>
            <staticContent>
                <remove fileExtension=".extension" />
                <mimeMap fileExtension=".extension" mimeType="application/example" />
            </staticContent>
        </system.webServer>
    </configuration>

For example, you might want to change the server level `.pdf` mime type
of `.pdf application/pdf` to `application/octet-stream`. Note that you
must include a `remove fileExtension` tag to avoid getting a 500 error.
We recommend that you add a `remove fileExtension` tag even if the
extension is not in our list. That way, if we ever add it to the server
level, it will not cause a 500 error because of a duplicate mime type
extension.

The following example shows the described change:

    <configuration>
    <system.webServer>
            <staticContent>
                <remove fileExtension=".pdf" />
                <mimeMap fileExtension=".pdf" mimeType="application/octet-stream" />
            </staticContent>
        </system.webServer>
    </configuration>

Following is the list of current mime types for our Windows Clusters:

- ".323" mimeType="text/h323"
- ".aaf" mimeType="application/octet-stream"
- ".aca" mimeType="application/octet-stream"
- ".accdb" mimeType="application/msaccess"
- ".accde" mimeType="application/msaccess"
- ".accdt" mimeType="application/msaccess"
- ".acx" mimeType="application/internet-property-stream"
- ".afm" mimeType="application/octet-stream"
- ".ai" mimeType="application/postscript"
- ".aif" mimeType="audio/x-aiff"
- ".aifc" mimeType="audio/aiff"
- ".aiff" mimeType="audio/aiff"
- ".application" mimeType="application/x-ms-application"
- ".art" mimeType="image/x-jg"
- ".asd" mimeType="application/octet-stream"
- ".asf" mimeType="video/x-ms-asf"
- ".asi" mimeType="application/octet-stream"
- ".asm" mimeType="text/plain"
- ".asr" mimeType="video/x-ms-asf"
- ".asx" mimeType="video/x-ms-asf"
- ".atom" mimeType="application/atom+xml"
- ".au" mimeType="audio/basic"
- ".avi" mimeType="video/x-msvideo"
- ".axs" mimeType="application/olescript"
- ".bas" mimeType="text/plain"
- ".bcpio" mimeType="application/x-bcpio"
- ".bin" mimeType="application/octet-stream"
- ".bmp" mimeType="image/bmp"
- ".c" mimeType="text/plain"
- ".cab" mimeType="application/octet-stream"
- ".calx" mimeType="application/vnd.ms-office.calx"
- ".cat" mimeType="application/vnd.ms-pki.seccat"
- ".cdf" mimeType="application/x-cdf"
- ".chm" mimeType="application/octet-stream"
- ".class" mimeType="application/x-java-applet"
- ".clp" mimeType="application/x-msclip"
- ".cmx" mimeType="image/x-cmx"
- ".cnf" mimeType="text/plain"
- ".cod" mimeType="image/cis-cod"
- ".cpio" mimeType="application/x-cpio"
- ".cpp" mimeType="text/plain"
- ".crd" mimeType="application/x-mscardfile"
- ".crl" mimeType="application/pkix-crl"
- ".crt" mimeType="application/x-x509-ca-cert"
- ".csh" mimeType="application/x-csh"
- ".css" mimeType="text/css"
- ".csv" mimeType="application/octet-stream"
- ".cur" mimeType="application/octet-stream"
- ".dcr" mimeType="application/x-director"
- ".deploy" mimeType="application/octet-stream"
- ".der" mimeType="application/x-x509-ca-cert"
- ".dib" mimeType="image/bmp"
- ".dir" mimeType="application/x-director"
- ".disco" mimeType="text/xml"
- ".dll" mimeType="application/x-msdownload"
- ".dll.config" mimeType="text/xml"
- ".dlm" mimeType="text/dlm"
- ".doc" mimeType="application/msword"
- ".docm" mimeType="application/vnd.ms-word.document.macroEnabled.12"
- ".docx" mimeType="application/vnd.openxmlformats-officedocument.wordprocessingml.document"
- ".dot" mimeType="application/msword"
- ".dotm" mimeType="application/vnd.ms-word.template.macroEnabled.12"
-  ".dotx" mimeType="application/vnd.openxmlformats-officedocument.wordprocessingml.template"
- ".dsp" mimeType="application/octet-stream"
- ".dtd" mimeType="text/xml"
- ".dvi" mimeType="application/x-dvi"
- ".dwf" mimeType="drawing/x-dwf"
- ".dwp" mimeType="application/octet-stream"
- ".dxr" mimeType="application/x-director"
- ".eml" mimeType="message/rfc822"
- ".emz" mimeType="application/octet-stream"
- ".eot" mimeType="application/octet-stream"
- ".eps" mimeType="application/postscript"
- ".etx" mimeType="text/x-setext"
- ".evy" mimeType="application/envoy"
- ".exe" mimeType="application/octet-stream"
- ".exe.config" mimeType="text/xml"
- ".fdf" mimeType="application/vnd.fdf"
- ".fif" mimeType="application/fractals"
- ".fla" mimeType="application/octet-stream"
- ".flr" mimeType="x-world/x-vrml"
- ".flv" mimeType="video/x-flv"
- ".gif" mimeType="image/gif"
- ".gtar" mimeType="application/x-gtar"
- ".gz" mimeType="application/x-gzip"
- ".h" mimeType="text/plain"
- ".hdf" mimeType="application/x-hdf"
- ".hdml" mimeType="text/x-hdml"
- ".hhc" mimeType="application/x-oleobject"
- ".hhk" mimeType="application/octet-stream"
- ".hhp" mimeType="application/octet-stream"
- ".hlp" mimeType="application/winhlp"
- ".hqx" mimeType="application/mac-binhex40"
- ".hta" mimeType="application/hta"
- ".htc" mimeType="text/x-component"
- ".htm" mimeType="text/html"
- ".html" mimeType="text/html"
- ".htt" mimeType="text/webviewhtml"
- ".hxt" mimeType="text/html"
- ".ico" mimeType="image/x-icon"
- ".ics" mimeType="application/octet-stream"
- ".ief" mimeType="image/ief"
- ".iii" mimeType="application/x-iphone"
- ".inf" mimeType="application/octet-stream"
- ".ins" mimeType="application/x-internet-signup"
- ".isp" mimeType="application/x-internet-signup"
- ".IVF" mimeType="video/x-ivf"
- ".jar" mimeType="application/java-archive"
- ".java" mimeType="application/octet-stream"
- ".jck" mimeType="application/liquidmotion"
- ".jcz" mimeType="application/liquidmotion"
- ".jfif" mimeType="image/pjpeg"
- ".jpb" mimeType="application/octet-stream"
- ".jpe" mimeType="image/jpeg"
- ".jpeg" mimeType="image/jpeg"
- ".jpg" mimeType="image/jpeg"
- ".js" mimeType="application/x-javascript"
- ".jsx" mimeType="text/jscript"
- ".latex" mimeType="application/x-latex"
- ".lit" mimeType="application/x-ms-reader"
- ".lpk" mimeType="application/octet-stream"
- ".lsf" mimeType="video/x-la-asf"
- ".lsx" mimeType="video/x-la-asf"
- ".lzh" mimeType="application/octet-stream"
- ".m13" mimeType="application/x-msmediaview"
- ".m14" mimeType="application/x-msmediaview"
- ".m1v" mimeType="video/mpeg"
- ".m3u" mimeType="audio/x-mpegurl"
- ".man" mimeType="application/x-troff-man"
- ".manifest" mimeType="application/x-ms-manifest"
- ".map" mimeType="text/plain"
- ".mdb" mimeType="application/x-msaccess"
- ".mdp" mimeType="application/octet-stream"
- ".me" mimeType="application/x-troff-me"
- ".mht" mimeType="message/rfc822"
- ".mhtml" mimeType="message/rfc822"
- ".mid" mimeType="audio/mid"
- ".midi" mimeType="audio/mid"
- ".mix" mimeType="application/octet-stream"
- ".mmf" mimeType="application/x-smaf"
- ".mno" mimeType="text/xml"
- ".mny" mimeType="application/x-msmoney"
- ".mov" mimeType="video/quicktime"
- ".movie" mimeType="video/x-sgi-movie"
- ".mp2" mimeType="video/mpeg"
- ".mp3" mimeType="audio/mpeg"
- ".mpa" mimeType="video/mpeg"
- ".mpe" mimeType="video/mpeg"
- ".mpeg" mimeType="video/mpeg"
- ".mpg" mimeType="video/mpeg"
- ".mpp" mimeType="application/vnd.ms-project"
- ".mpv2" mimeType="video/mpeg"
- ".ms" mimeType="application/x-troff-ms"
- ".msi" mimeType="application/octet-stream"
- ".mso" mimeType="application/octet-stream"
- ".mvb" mimeType="application/x-msmediaview"
- ".mvc" mimeType="application/x-miva-compiled"
- ".nc" mimeType="application/x-netcdf"
- ".nsc" mimeType="video/x-ms-asf"
- ".nws" mimeType="message/rfc822"
- ".ocx" mimeType="application/octet-stream"
- ".oda" mimeType="application/oda"
- ".odc" mimeType="text/x-ms-odc"
- ".ods" mimeType="application/oleobject"
- ".one" mimeType="application/onenote"
- ".onea" mimeType="application/onenote"
- ".onetoc" mimeType="application/onenote"
- ".onetoc2" mimeType="application/onenote"
- ".onetmp" mimeType="application/onenote"
- ".onepkg" mimeType="application/onenote"
- ".p10" mimeType="application/pkcs10"
- ".p12" mimeType="application/x-pkcs12"
- ".p7b" mimeType="application/x-pkcs7-certificates"
- ".p7c" mimeType="application/pkcs7-mime"
- ".p7m" mimeType="application/pkcs7-mime"
- ".p7r" mimeType="application/x-pkcs7-certreqresp"
- ".p7s" mimeType="application/pkcs7-signature"
- ".pbm" mimeType="image/x-portable-bitmap"
- ".pcx" mimeType="application/octet-stream"
- ".pcz" mimeType="application/octet-stream"
- ".pdf" mimeType="application/pdf"
- ".pfb" mimeType="application/octet-stream"
- ".pfm" mimeType="application/octet-stream"
- ".pfx" mimeType="application/x-pkcs12"
- ".pgm" mimeType="image/x-portable-graymap"
- ".pko" mimeType="application/vnd.ms-pki.pko"
- ".pma" mimeType="application/x-perfmon"
- ".pmc" mimeType="application/x-perfmon"
- ".pml" mimeType="application/x-perfmon"
- ".pmr" mimeType="application/x-perfmon"
- ".pmw" mimeType="application/x-perfmon"
- ".png" mimeType="image/png"
- ".pnm" mimeType="image/x-portable-anymap"
- ".pnz" mimeType="image/png"
- ".pot" mimeType="application/vnd.ms-powerpoint"
- ".potm" mimeType="application/vnd.ms-powerpoint.template.macroEnabled.12"
- ".potx" mimeType="application/vnd.openxmlformats-officedocument.presentationml.template"
- ".ppam" mimeType="application/vnd.ms-powerpoint.addin.macroEnabled.12"
- ".ppm" mimeType="image/x-portable-pixmap"
- ".pps" mimeType="application/vnd.ms-powerpoint"
- ".ppsm" mimeType="application/vnd.ms-powerpoint.slideshow.macroEnabled.12"
- ".ppsx" mimeType="application/vnd.openxmlformats-officedocument.presentationml.slideshow"
- ".ppt" mimeType="application/vnd.ms-powerpoint"
- ".pptm" mimeType="application/vnd.ms-powerpoint.presentation.macroEnabled.12"
- ".pptx" mimeType="application/vnd.openxmlformats-officedocument.presentationml.presentation"
- ".prf" mimeType="application/pics-rules"
- ".prm" mimeType="application/octet-stream"
- ".prx" mimeType="application/octet-stream"
- ".ps" mimeType="application/postscript"
- ".psd" mimeType="application/octet-stream"
- ".psm" mimeType="application/octet-stream"
- ".psp" mimeType="application/octet-stream"
- ".pub" mimeType="application/x-mspublisher"
- ".qt" mimeType="video/quicktime"
- ".qtl" mimeType="application/x-quicktimeplayer"
- ".qxd" mimeType="application/octet-stream"
- ".ra" mimeType="audio/x-pn-realaudio"
- ".ram" mimeType="audio/x-pn-realaudio"
- ".rar" mimeType="application/octet-stream"
- ".ras" mimeType="image/x-cmu-raster"
- ".rf" mimeType="image/vnd.rn-realflash"
- ".rgb" mimeType="image/x-rgb"
- ".rm" mimeType="application/vnd.rn-realmedia"
- ".rmi" mimeType="audio/mid"
- ".roff" mimeType="application/x-troff"
- ".rpm" mimeType="audio/x-pn-realaudio-plugin"
- ".rtf" mimeType="application/rtf"
- ".rtx" mimeType="text/richtext"
- ".scd" mimeType="application/x-msschedule"
- ".sct" mimeType="text/scriptlet"
- ".sea" mimeType="application/octet-stream"
- ".setpay" mimeType="application/set-payment-initiation"
- ".setreg" mimeType="application/set-registration-initiation"
- ".sgml" mimeType="text/sgml"
- ".sh" mimeType="application/x-sh"
- ".shar" mimeType="application/x-shar"
- ".sit" mimeType="application/x-stuffit"
- ".sldm" mimeType="application/vnd.ms-powerpoint.slide.macroEnabled.12"
- ".sldx" mimeType="application/vnd.openxmlformats-officedocument.presentationml.slide"
- ".smd" mimeType="audio/x-smd"
- ".smi" mimeType="application/octet-stream"
- ".smx" mimeType="audio/x-smd"
- ".smz" mimeType="audio/x-smd"
- ".snd" mimeType="audio/basic"
- ".snp" mimeType="application/octet-stream"
- ".spc" mimeType="application/x-pkcs7-certificates"
- ".spl" mimeType="application/futuresplash"
- ".src" mimeType="application/x-wais-source"
- ".ssm" mimeType="application/streamingmedia"
- ".sst" mimeType="application/vnd.ms-pki.certstore"
- ".stl" mimeType="application/vnd.ms-pki.stl"
- ".sv4cpio" mimeType="application/x-sv4cpio"
- ".sv4crc" mimeType="application/x-sv4crc"
- ".swf" mimeType="application/x-shockwave-flash"
- ".t" mimeType="application/x-troff"
- ".tar" mimeType="application/x-tar"
- ".tcl" mimeType="application/x-tcl"
- ".tex" mimeType="application/x-tex"
- ".texi" mimeType="application/x-texinfo"
- ".texinfo" mimeType="application/x-texinfo"
- ".tgz" mimeType="application/x-compressed"
- ".thmx" mimeType="application/vnd.ms-officetheme"
- ".thn" mimeType="application/octet-stream"
- ".tif" mimeType="image/tiff"
- ".tiff" mimeType="image/tiff"
- ".toc" mimeType="application/octet-stream"
- ".tr" mimeType="application/x-troff"
- ".trm" mimeType="application/x-msterminal"
- ".tsv" mimeType="text/tab-separated-values"
- ".ttf" mimeType="application/octet-stream"
- ".txt" mimeType="text/plain"
- ".u32" mimeType="application/octet-stream"
- ".uls" mimeType="text/iuls"
- ".ustar" mimeType="application/x-ustar"
- ".vbs" mimeType="text/vbscript"
- ".vcf" mimeType="text/x-vcard"
- ".vcs" mimeType="text/plain"
- ".vdx" mimeType="application/vnd.ms-visio.viewer"
- ".vml" mimeType="text/xml"
- ".vsd" mimeType="application/vnd.visio"
- ".vss" mimeType="application/vnd.visio"
- ".vst" mimeType="application/vnd.visio"
- ".vsto" mimeType="application/x-ms-vsto"
- ".vsw" mimeType="application/vnd.visio"
- ".vsx" mimeType="application/vnd.visio"
- ".vtx" mimeType="application/vnd.visio"
- ".wav" mimeType="audio/wav"
- ".wax" mimeType="audio/x-ms-wax"
- ".wbmp" mimeType="image/vnd.wap.wbmp"
- ".wcm" mimeType="application/vnd.ms-works"
- ".wdb" mimeType="application/vnd.ms-works"
- ".wks" mimeType="application/vnd.ms-works"
- ".wm" mimeType="video/x-ms-wm"
- ".wma" mimeType="audio/x-ms-wma"
- ".wmd" mimeType="application/x-ms-wmd"
- ".wmf" mimeType="application/x-msmetafile"
- ".wml" mimeType="text/vnd.wap.wml"
- ".wmlc" mimeType="application/vnd.wap.wmlc"
- ".wmls" mimeType="text/vnd.wap.wmlscript"
- ".wmlsc" mimeType="application/vnd.wap.wmlscriptc"
- ".wmp" mimeType="video/x-ms-wmp"
- ".wmv" mimeType="video/x-ms-wmv"
- ".wmx" mimeType="video/x-ms-wmx"
- ".wmz" mimeType="application/x-ms-wmz"
- ".wps" mimeType="application/vnd.ms-works"
- ".wri" mimeType="application/x-mswrite"
- ".wrl" mimeType="x-world/x-vrml"
- ".wrz" mimeType="x-world/x-vrml"
- ".wsdl" mimeType="text/xml"
- ".wvx" mimeType="video/x-ms-wvx"
- ".x" mimeType="application/directx"
- ".xaf" mimeType="x-world/x-vrml"
- ".xaml" mimeType="application/xaml+xml"
- ".xap" mimeType="application/x-silverlight-app"
- ".xbap" mimeType="application/x-ms-xbap"
- ".xbm" mimeType="image/x-xbitmap"
- ".xdr" mimeType="text/plain"
- ".xla" mimeType="application/vnd.ms-excel"
- ".xlam" mimeType="application/vnd.ms-excel.addin.macroEnabled.12"
- ".xlc" mimeType="application/vnd.ms-excel"
- ".xlm" mimeType="application/vnd.ms-excel"
- ".xls" mimeType="application/vnd.ms-excel"
- ".xlsb" mimeType="application/vnd.ms-excel.sheet.binary.macroEnabled.12"
- ".xlsm" mimeType="application/vnd.ms-excel.sheet.macroEnabled.12"
- ".xlsx" mimeType="application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
- ".xlt" mimeType="application/vnd.ms-excel"
- ".xltm" mimeType="application/vnd.ms-excel.template.macroEnabled.12"
- ".xltx" mimeType="application/vnd.openxmlformats-officedocument.spreadsheetml.template"
- ".xlw" mimeType="application/vnd.ms-excel"
- ".xml" mimeType="text/xml"
- ".xof" mimeType="x-world/x-vrml"
- ".xpm" mimeType="image/x-xpixmap"
- ".xps" mimeType="application/vnd.ms-xpsdocument"
- ".xsd" mimeType="text/xml"
- ".xsf" mimeType="text/xml"
- ".xsl" mimeType="text/xml"
- ".xslt" mimeType="text/xml"
- ".xsn" mimeType="application/octet-stream"
- ".xtp" mimeType="application/octet-stream"
- ".xwd" mimeType="image/x-xwindowdump"
- ".z" mimeType="application/x-compress"
- ".zip" mimeType="application/x-zip-compressed"
- ".php" mimeType="redirect/php"
- ".7z" mimeType="application/x-7z-compressed"
- ".kml" mimeType="application/vnd.google-earth.kml+xml"
- ".kmz" mimeType="application/vnd.google-earth.kmz"
- ".svg" mimeType="image/svg xml"
- ".mp4" mimeType="video/mp4"
- ".m4v" mimeType="video/mp4"
- ".xpi" mimeType="application/x-xpinstall"
- ".air" mimeType="application/vnd.adobe.air-application-installer-package+zip"
