# IMSC-1.1_Text_TestContent

This reel is a continuation of the IMSC-1.0.1_Text_TestContent assets. This reel was created with the same scope as the original reel, where the items that are tested are all pertinent to subtitles produced for production content. This version adds numerous additional tests that focus on foreign language rendering, color compositing to different color spaces, and some new IMSC 1.1 attributes. Like the original reel, this has been built to help manufacturers with their IMSC 1.1 Text implementations by providing them with a reference IMSC package.

This test content includes the following assets:

IMSC1-1_TEXT_Test-Reel_FMS_v3-0_2019-01-29.xml
IMSC1-1_TEXT_Test-Reel_FMS_v3-0_2019-01-29_Rec709_Backplate.mov*
IMSC1-1_TEXT_Test-Reel_FMS_v3-0_2019-01-29_Rec709_CompositedProxy.mp4*
IMSC1-1_TEXT_Test-Reel_FMS_v3-0_2019-01-29_Rec2020-PQ_Backplate.mov*
IMSC1-1_TEXT_Test-Reel_FMS_v3-0_2019-01-29_Rec2020-PQ_CompositedProxy.mp4*
*Please note that these media files are hosted at https://foxgroup.box.com/, and are linked to via .URL  internet shortcut files.

The IMSC XML file is to be rendered over the Backplate ProRes HQ file. If the IMSC decoding is accurate, it will look approximately the same as the Composited Proxy file. It is acceptable for there to be slight differences in text rendering, since the proportionalSansSerif font chosen by the renderer may be different than what was used for the proxy. There is both a Rec 709 backplate and proxy, along with a Rec 2020 PQ backplate and proxy. The recommended approach for compositing sRGB subtitles to rec 709 and rec 2020 PQ is:

    sRGB (EOTF 2.4) to 709 Full Range (EOTF 2.4)
    No conversion is required.

    sRGB (EOTF 2.4) to 709 Narrow Range (EOTF 2.4)
    Scale the sRGB values to narrow range as described in section 6 of RP 2077:2013.

    sRGB (EOTF 2.4) to PQ 2020 Full Range (EOTF PQ)
    Map the sRGB values to PQ 2020 Full Range as described in section Q.1 of the TTML2 Recommendation.

    sRGB (EOTF 2.4) to PQ 2020 Narrow Range (EOTF PQ)
    Map the sRGB values to PQ 2020 Full Range as described in section Q.1 of the TTML2 Recommendation,
    then scale those values to narrow range as described in section 6 of RP 2077:2013.

The IMSC 1.1 XML file includes in-line comments which describes the purpose of each test.

The backplate includes the following:
- Grid with lines every 5%
- Yellow crosses at each corner of the region
- Sync counter at the beginning and end of each event
