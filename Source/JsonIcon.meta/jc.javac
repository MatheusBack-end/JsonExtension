public class JsonIcon extends FilesPanelCustomIcon
{
    private String icon_path = "Files/EditorExtensionJson/Assets/json_file_icon.png";

    @Override
    public File getIconForFile(File file)
    {
        return new File(Directories.getProjectFolder() + icon_path);
    }

    @Override
    public boolean supportFile(File file)
    {
      return file.getAbsolutePath().endsWith(".json");
    }
}
