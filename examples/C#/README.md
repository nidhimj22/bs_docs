## Session ID 

To get the session ID of a session 
` var sessionIdProperty = typeof(RemoteWebDriver).GetProperty("SessionId", BindingFlags.Instance | BindingFlags.NonPublic);
  SessionId sessionId = sessionIdProperty.GetValue(driver, null) as SessionId;
  Console.WriteLine(sessionId.ToString()); `