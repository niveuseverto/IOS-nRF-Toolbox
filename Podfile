target 'nRF Toolbox' do
  use_frameworks!

  pod 'Zip', :git => 'git@github.com:marmelroy/Zip.git', :branch => 'swift2.3', :submodules => true
  
  pod 'iOSDFULibrary', :git => 'git@github.com:niveuseverto/IOS-Pods-DFU-Library', :branch => 'swift2.3'
  pod 'SWRevealViewController', '~> 2.3'
  pod 'CorePlot', :git => 'git@github.com:core-plot/core-plot.git', :branch => 'release-2.2'
  pod 'EVReflection', :git => 'git@github.com:evermeer/EVReflection.git', :branch => 'Swift3'

  target 'nRF ToolboxTests' do
    inherit! :search_paths
  end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '2.3'
    end
  end
end
  
end
