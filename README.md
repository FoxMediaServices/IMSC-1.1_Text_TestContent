# IMSC-1.1_Text_TestContent

This reel is a continuation of the IMSC-1.0.1_Text_TestContent assets. This reel was created with the same scope as the original reel, where the items that are tested are all pertinent to subtitles produced for production content. This version adds numerous additional tests that focus on foreign language rendering, color compositing to different color spaces, and some new IMSC 1.1 attributes. Like the original reel, this has been built to help manufacturers with their IMSC 1.1 Text implementations by providing them with a reference IMSC package.

This test content includes the following assets:
- IMSC1-1_TEXT_Test-Reel_FMS_v4-0-1_2019-11-20.xml
- IMSC1-1_TEXT_Test-Reel_FMS_v4-0_2019-11-20_HLG_Backplate.mxf*
- IMSC1-1_TEXT_Test-Reel_FMS_v4-0_2019-11-20_HLG_CompositedProxy.mov*
- IMSC1-1_TEXT_Test-Reel_FMS_v4-0_2019-11-20_Rec2020-PQ_Backplate.mxf*
- IMSC1-1_TEXT_Test-Reel_FMS_v4-0_2019-11-20_Rec2020-PQ_CompositedProxy.mov*
- IMSC1-1_TEXT_Test-Reel_FMS_v4-0_2019-11-20_Rec709_Backplate.mxf*
- IMSC1-1_TEXT_Test-Reel_FMS_v4-0_2019-11-20_Rec709_CompositedProxy.mov*

    **These files can be found at the w3c fork of this repo: https://github.com/w3c/IMSC-1.1_Text_TestContent*

The IMSC XML file is to be rendered over the Backplate MXF file. If the IMSC decoding is accurate, it will look approximately the same as the Composited Proxy file. It is acceptable for there to be slight differences in text rendering, since the proportionalSansSerif font chosen by the renderer may be different than what was used for the proxy. There is a Rec 709 backplate and proxy, a Rec 2020 PQ backplate and proxy, and an HLG backplate and proxy. The recommended approach for compositing sRGB subtitles to rec 709, rec 2020 PQ, and HLG is:

    sRGB (EOTF 2.2) to 709 (EOTF 2.4)
    Map the sRGB values from an EOTF of 2.2 to an EOTF of 2.4

    sRGB (EOTF 2.2) to PQ 2020 (EOTF PQ)
    Map the sRGB values to PQ 2020 as described in section Q.1 of the Draft TTML2 Recommendation

    sRGB (EOTF 2.0) to HLG
    Map the sRGB values to PQ 2020 as described in section Q.2 of the Draft TTML2 Recommendation

The IMSC 1.1 XML file includes in-line comments which describes the purpose of each test.

The backplate includes the following:
- Frame counter and Media Time counter
- Grid with lines every 5%
- Yellow crosses at each corner of the region
- Sync counter at the beginning and end of each event
