public class JsonEditor extends TextScriptingExtension
{
    private File current_file;
    
    @Override
    public void init()
    {
        super.setStyler(new JsonStyler());
        super.setTheme(new JsonTheme().get());
    }
    
    @Override
    public void openScript(File file)
    {
        String json_contents = "";
        
        try
        {
            json_contents = FileLoader.loadTextFromFile(file);
            
            // TODO: format json
            // JsonElement element = Json.toElement(json_contents);
        }
        
        catch(Exception e)
        {
            Console.log(e);
        }
        
        current_file = file;
        setText(json_contents);
    }
    
    @Override
    public boolean saveScript()
    {
        try
        {
            FileLoader.exportTextToFile(getText(), current_file);
            return true;
        }
        
        catch(Exception e)
        {
            Console.log(e);
        }
        
        return false;
    }
    
    @Override
    public boolean supportFile(File file)
    {
        return file.getAbsolutePath().endsWith(".json");
    }
}
