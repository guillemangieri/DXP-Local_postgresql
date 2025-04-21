FROM liferay/dxp:7.4.13-u75

# Copia a chave de autenticação para a pasta deploy
COPY deploy/activation-key-dxpdevelopment-7.4-mti-migrationfromportaltoliferaydxp.xml $LIFERAY_HOME/deploy/

# Copia o arquivo de configuração do Liferay
COPY portal-ext.properties $LIFERAY_HOME/

# Garante permissões corretas (usuário padrão do Liferay: liferay)
USER root
RUN chown -R liferay:liferay $LIFERAY_HOME/
USER liferay

# Porta exposta
EXPOSE 8080

CMD ["catalina.sh", "run"]