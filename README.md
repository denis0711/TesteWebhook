# TesteWebhook



Testando o Push



Meu script webhook



[HttpPost("webhook")]
[AllowAnonymous]
public IActionResult ReceberWebhook([FromBody] Webhook payload)
{
    // Executar ação na API com base nos dados recebidos pelo webhook.
    MinhaAcao(payload);

    return Ok();
}

private async void MinhaAcao(Webhook payload)
{
    var resultado = await  service.CreateAsync(payload);
    
}