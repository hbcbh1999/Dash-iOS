platform :ios, "9.0"
inhibit_all_warnings!

target "Dash" do
    pod 'MRProgress', :path => 'Modified Pods/MRProgress/MRProgress.podspec'
    # Commented out a bunch of stuff in MRBlurView's redraw, otherwise the overlay progress makes the entire screen flicker when it is first shown
    # MRStopButton has support for whole sizes (their calculations ended up with non-integral frames)
    # Also overwrote pointInside: for MRCircularProgressView...
    # Removed AccessibilityValueChangeNotify because it causes VoiceOver to stall
    pod 'KissXML'
    pod 'UIAlertView+Blocks'
    pod 'UIActionSheet+Blocks'
    pod 'AutoCoding'
#    pod 'HockeySDK'
    pod 'DZNEmptyDataSet', :path => 'Modified Pods/DZNEmptyDataSet/DZNEmptyDataSet.podspec'
    # Some changes in terms of repositioning after orientation change
    pod 'JGMethodSwizzler'
    pod 'DTBonjour', :path => 'Modified Pods/DTBonjour/DTBonjour.podspec'
    # Modified to add originating IP address support to DTBonjourDataConnection
    # Also modified to send a delegate message when a connection closes
    # Replaced asserts() with ifs() in DTBonjourServer start
    
    pod 'Reachability'
    pod 'SAMKeychain'
    pod 'NSTimer-Blocks'
    pod 'GZIP'
end

post_install do | installer |
    require 'fileutils'
    FileUtils.cp_r('Pods/Target Support Files/Pods-Dash/Pods-Dash-acknowledgements.plist', 'Dash/Settings.bundle/Cocoa_Pods_Acknowledgements.plist', :remove_destination => true)
end
