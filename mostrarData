import java.time.LocalDate;
import java.time.LocalTime;
import java.time.format.DateTimeFormatter;
import java.time.format.FormatStyle;
import java.time.format.TextStyle;
import java.util.Locale;
import java.time.DayOfWeek;

public class mostrarData {
    public static void main(String[] args) {
        LocalDate dataHoje = LocalDate.now();

        String dataFormatada = formatarData(dataHoje);
        System.out.println(dataFormatada);
    }

    public static String formatarData(LocalDate data) {
        DayOfWeek diaSemana = data.getDayOfWeek();
        String nDiaSemana = diaSemana.getDisplayName(
            TextStyle.FULL, Locale.forLanguageTag("pt-BR")
        );

        DateTimeFormatter formatter = DateTimeFormatter.ofLocalizedDate(FormatStyle.LONG);
        String dataFormatada = data.format(formatter);

        int hr = LocalTime.now().getHour();
        int min = LocalTime.now().getMinute();

        String comoFicou = String.format(
            "Hoje é %s, dia %02d de %s de %d com o horário de %02d horas e %02d minutos.",
            nDiaSemana, data.getDayOfMonth(), data.getMonth().getDisplayName(TextStyle.FULL, Locale.forLanguageTag("pt-BR")),
            data.getYear(), hr, min
        );

        return comoFicou;
    }
}
